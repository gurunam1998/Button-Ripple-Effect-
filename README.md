# Button-Ripple-Effect-
Button Ripple Effect using HTML, CSS and Javascript

# Introduction of Button-Ripple-Effect-
The Button Ripple Effect is a visually appealing UI interaction where a ripple-like animation spreads outward when a button is clicked. This effect enhances user experience by providing immediate feedback on interactions.
The ripple effect is commonly used in modern web design, especially in Material Design principles. It creates a dynamic wave effect when a user clicks on a button, making the interface feel more interactive.

How It Works
- HTML Structure – A simple button element is created.
- CSS Styling – The button is styled with animations and transitions.
- JavaScript Implementation – JavaScript detects the click position and generates a ripple effect dynamically.

Example Implementation
Here’s another basic example of how you can create a button ripple effect:
<button class="ripple-button">Click Me</button>


.ripple-button {
  position: relative;
  overflow: hidden;
  background-color: #6200ea;
  color: white;
  padding: 15px 30px;
  border: none;
  cursor: pointer;
}

.ripple-button::after {
  content: "";
  position: absolute;
  width: 100px;
  height: 100px;
  background: rgba(255, 255, 255, 0.5);
  border-radius: 50%;
  transform: scale(0);
  animation: ripple-animation 0.6s linear;
}

@keyframes ripple-animation {
  to {
    transform: scale(4);
    opacity: 0;
  }
}


document.querySelector(".ripple-button").addEventListener("click", function (e) {
  let ripple = document.createElement("span");
  ripple.classList.add("ripple");
  this.appendChild(ripple);

  let x = e.clientX - this.offsetLeft;
  let y = e.clientY - this.offsetTop;

  ripple.style.left = `${x}px`;
  ripple.style.top = `${y}px`;

  setTimeout(() => {
    ripple.remove();
  }, 600);
});


This effect is widely used in UI/UX design to make buttons more engaging. You can explore more details and variations here and here. Let me know if you need further guidance! 🚀
