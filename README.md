## Hi there 👋

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>GSAP Text Animation</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      font-size: 2em;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #111;
      color: white;
    }
    .text span {
      display: inline-block;
      opacity: 0;
      transform: translateY(20px);
    }
  </style>
</head>
<body>

  <div class="text">Hello Kalpesh!</div>

  <script>
    const text = document.querySelector('.text');
    const chars = text.textContent.split('');
    text.textContent = '';

    chars.forEach(char => {
      const span = document.createElement('span');
      span.textContent = char;
      text.appendChild(span);
    });

    gsap.to('.text span', {
      opacity: 1,
      y: 0,
      stagger: 0.05,
      duration: 0.6,
      ease: 'power2.out'
    });
  </script>

</body>
</html>


