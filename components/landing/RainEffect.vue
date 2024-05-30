<template>
  <canvas ref="rainCanvas" class="rainy-container"></canvas>
</template>

<script>
export default {
  mounted() {
    this.initRainEffect();
  },
  methods: {
// В методе mounted вашего компонента Vue
    initRainEffect() {
      const canvas = this.$refs.rainCanvas;
      const ctx = canvas.getContext('2d');

      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;

      const drops = [];
      for (let i = 0; i < 100; i++) {
        drops.push({
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height,
          speed: 1 + Math.random() * 2,
          length: Math.random() * 20 + 10
        });
      }

      const animate = () => {
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Изменение цвета капель на светло-серый
        ctx.strokeStyle = 'rgba(150, 150, 150, 0.5)';

        for (const drop of drops) {
          ctx.beginPath();
          ctx.moveTo(drop.x, drop.y);
          ctx.lineTo(drop.x, drop.y + drop.length);
          ctx.stroke();
          drop.y += drop.speed;
          if (drop.y > canvas.height) {
            drop.y = -drop.length;
          }
        }

        requestAnimationFrame(animate);
      };

      animate();
    }

  }
};
</script>

<style scoped>
.rainy-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}
</style>
