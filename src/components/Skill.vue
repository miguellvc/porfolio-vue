<script setup>
</script>

<template>
    <section id="habilidades" class="habilidades">
        <h1 class="section_title">Habilidades</h1>

        <div class="tools-container">
            <div class="tools-grid">
                <div class="tool-item">
                    <span class="tool-icon"><img src="../assets/img/js.png" alt="git" class="img"></span>
                    <div class="tool-name">JavaScript</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/visual-basico.png" alt="git" class="img"></span>
                    <div class="tool-name">VS Code</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/git.png" alt="git" class="img"></span>
                    <div class="tool-name">Git</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/github.png" alt="github" class="img"></span>
                    <div class="tool-name">Github</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/java.png" alt="github" class="img"></span>
                    <div class="tool-name">Java</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/piton.png" alt="python" class="img"></span>
                    <div class="tool-name">Python</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/css-3.png" alt="css" class="img"></span>
                    <div class="tool-name">CSS</div>
                </div>

                <div class="tool-item">
                    <span class="tool-icon"><img src="./src/img/html.png" alt="html" class="img"></span>
                    <div class="tool-name">HTML</div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>

.tools-container {
  padding: 2.5rem;

}


.category-icon {
  width: 40px;
  height: 40px;
  background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.2rem;
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 6rem;
  justify-items: center;
}

.tool-item {
  background: rgba(255, 255, 255, 0.15);
  border-radius: 16px;
  padding: 2rem 2rem;
  text-align: center;
  transition: all 0.3s ease;
  border: 1px solid rgba(255, 255, 255, 0.2);
  width: 100%;
  max-width: 160px;
  position: relative;
  overflow: hidden;
}

.tool-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
  transition: left 0.5s ease;
}

.tool-item:hover::before {
  left: 100%;
}

.tool-item:hover {
  background: rgba(255, 255, 255, 0.25);
  transform: translateY(-8px) scale(1.05);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}

.tool-icon {
  font-size: 5rem;
  margin-bottom: 0.8rem;
  display: block;
  transition: transform 0.3s ease;
}

.tool-icon .img {
  width: 60px;
}

.tool-item:hover .tool-icon {
  transform: scale(1.1) rotate(5deg);
}

.tool-name {
  color: white;
  font-size: 1.5rem;
  font-weight: 600;
  letter-spacing: 0.5px;
}

/* Responsive Design */
@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }

  .tools-container {
    padding: 2rem 1.5rem;
  }

  .tools-grid {
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    gap: 1.2rem;
  }

  .tool-item {
    padding: 1.2rem 0.8rem;
    max-width: 140px;
  }

}

@media (max-width: 480px) {
  .tools-section {
    padding: 0 1rem;
  }

  .section-title {
    font-size: 1.8rem;
  }

  .tools-grid {
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 5rem;
  }

  .tool-item {
    padding: 2rem 2rem;
    max-width: 120px;
  }

  .category-title {
    font-size: 1.5rem;
    flex-direction: column;
    gap: 0.5rem;
  }
}

/* Animaciones de entrada */
.tools-container {
  opacity: 0;
  transform: translateY(30px);
  animation: fadeInUp 0.8s ease forwards;
}

.tool-item {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.6s ease forwards;
}

.tool-item:nth-child(1) {
  animation-delay: 0.1s;
}

.tool-item:nth-child(2) {
  animation-delay: 0.2s;
}

.tool-item:nth-child(3) {
  animation-delay: 0.3s;
}

.tool-item:nth-child(4) {
  animation-delay: 0.4s;
}

.tool-item:nth-child(5) {
  animation-delay: 0.5s;
}

.tool-item:nth-child(6) {
  animation-delay: 0.6s;
}

.tool-item:nth-child(7) {
  animation-delay: 0.7s;
}

.tool-item:nth-child(8) {
  animation-delay: 0.8s;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

</style>