/* Add these styles to your existing CSS */

/* Hover Effects for Countdown Boxes */
.countdown div {
  transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease;
}

.countdown div:hover {
  transform: translateY(-10px) scale(1.05);
  box-shadow: 0 15px 30px rgba(255, 255, 255, 0.4);
  background: rgba(255, 255, 255, 0.2);
}

/* Pulse Animation for Countdown Numbers */
@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

.countdown div span {
  animation: pulse 2s infinite;
}

/* Gradient Border Animation */
.countdown div {
  position: relative;
  overflow: hidden;
}

.countdown div::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(45deg, #ff9a9e, #fad0c4, #fbc2eb, #a6c1ee);
  z-index: -1;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.countdown div:hover::before {
  opacity: 0.3;
}

/* Floating Animation for Particles */
@keyframes float {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0);
  }
}

body::before {
  animation: moveBackground 5s linear infinite, float 6s ease-in-out infinite;
}

/* Glow Effect for Icons */
.countdown i {
  transition: text-shadow 0.3s ease;
}

.countdown div:hover i {
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.8), 0 0 20px rgba(255, 255, 255, 0.6);
}

/* Footer Hover Effect */
footer {
  transition: opacity 0.3s ease, transform 0.3s ease;
}

footer:hover {
  opacity: 1;
  transform: translateY(-5px);
}

/* Visitor Counter Animation */
.visitor-count {
  transition: transform 0.3s ease;
}

.visitor-count:hover {
  transform: scale(1.1);
}

/* Responsive Adjustments */
@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }

  .bac-section {
    font-size: 2.5rem;
  }

  .countdown {
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }

  .countdown div {
    width: 80%;
    padding: 15px;
  }

  .countdown span {
    font-size: 1rem;
  }

  .countdown i {
    font-size: 1.5rem;
  }
}