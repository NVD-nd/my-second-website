<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lời tỏ tình đặc biệt</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #ff4d6d;
      --secondary-color: #ff8fa3;
      --accent-color: #ffb3c1;
      --text-color: #2b2d42;
      --light-color: #fff0f3;
    }
    
    body {
      margin: 0;
      padding: 0;
      min-height: 100vh;
      overflow-x: hidden;
      background: linear-gradient(135deg, var(--light-color), #ffffff);
      font-family: 'Montserrat', sans-serif;
      text-align: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
    }
    
    .container {
      max-width: 800px;
      padding: 2rem;
      background-color: rgba(255, 255, 255, 0.9);
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      z-index: 10;
      backdrop-filter: blur(5px);
      margin: 2rem;
      transition: transform 0.3s ease;
    }
    
    .container:hover {
      transform: translateY(-5px);
    }
    
    h1 {
      margin: 0;
      font-family: 'Dancing Script', cursive;
      font-size: 3.5rem;
      color: var(--primary-color);
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
      line-height: 1.2;
    }
    
    p {
      font-size: 1.5rem;
      color: var(--text-color);
      margin: 1.5rem 0;
      font-weight: 600;
    }
    
    .buttons {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin-top: 2rem;
    }
    
    button {
      padding: 1rem 2rem;
      font-size: 1.2rem;
      border: none;
      border-radius: 50px;
      background-color: var(--primary-color);
      color: white;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      font-weight: 600;
      min-width: 180px;
      position: relative;
      overflow: hidden;
    }
    
    button::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
      transition: 0.5s;
    }
    
    button:hover {
      background-color: var(--secondary-color);
      transform: translateY(-3px);
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
    }
    
    button:hover::before {
      left: 100%;
    }
    
    button:active {
      transform: translateY(1px);
    }
    
    #noBtn {
      background-color: #f8f9fa;
      color: var(--text-color);
    }
    
    #noBtn:hover {
      background-color: #e9ecef;
    }
    
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: var(--accent-color);
      transform: rotate(45deg);
      animation: float 8s linear infinite;
      opacity: 0;
      z-index: 1;
    }
    
    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: var(--accent-color);
      border-radius: 50%;
    }
    
    .heart::before {
      top: -10px;
      left: 0;      
    }
    
    .heart::after {
      left: -10px;
      top: 0;
    }
    
    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg) scale(0.5);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(45deg) scale(1.2);
        opacity: 0;
      }
    }
    
    .floating-hearts {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }
    
    .photo-frame {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 5px solid var(--primary-color);
      margin: 0 auto 1.5rem;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }
    
    .photo-frame:hover {
      transform: rotate(10deg) scale(1.05);
    }
    
    .photo-frame img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .confetti {
      position: fixed;
      width: 10px;
      height: 10px;
      background-color: var(--primary-color);
      opacity: 0;
      z-index: 100;
      animation: confetti-fall 3s ease-in-out forwards;
    }
    
    @keyframes confetti-fall {
      0% {
        transform: translateY(-100px) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
    
    @media (max-width: 768px) {
      h1 {
        font-size: 2.5rem;
      }
      
      p {
        font-size: 1.2rem;
      }
      
      .container {
        margin: 1rem;
        padding: 1.5rem;
      }
      
      button {
        min-width: 140px;
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <div class="floating-hearts" id="heartsContainer"></div>
  
  <div class="container">
    <div class="photo-frame">
      <img src="https://i.imgur.com/JqYeYnN.jpg" alt="Ảnh của chúng ta">
    </div>
    
    <h1>Em có muốn trở thành một nửa của anh không?</h1>
    <p>Anh sẽ luôn ở bên em, dù là hôm nay, ngày mai hay mãi mãi ❤️</p>
    
    <div class="buttons">
      <button id="yesBtn">Có, em đồng ý!</button>
      <button id="noBtn">Anh xứng đáng hơn thế...</button>
    </div>
  </div>

  <audio id="bgMusic" loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    Trình duyệt của bạn không hỗ trợ audio.
  </audio>

  <script>
    // Tạo trái tim bay
    function createHearts() {
      const heartsContainer = document.getElementById('heartsContainer');
      const heart = document.createElement('div');
      heart.className = 'heart';
      
      // Random vị trí và kích thước
      const size = Math.random() * 20 + 10;
      heart.style.width = `${size}px`;
      heart.style.height = `${size}px`;
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (4 + Math.random() * 6) + 's';
      heart.style.animationDelay = Math.random() * 5 + 's';
      
      // Random màu sắc
      const colors = ['#ff4d6d', '#ff8fa3', '#ffb3c1', '#ffccd5'];
      heart.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
      
      heartsContainer.appendChild(heart);
      
      // Tự động xóa sau khi animation kết thúc
      setTimeout(() => {
        heart.remove();
      }, 10000);
    }
    
    // Tạo confetti
    function createConfetti() {
      for (let i = 0; i < 100; i++) {
        const confetti = document.createElement('div');
        confetti.className = 'confetti';
        
        // Random vị trí, màu sắc và hình dạng
        confetti.style.left = Math.random() * 100 + 'vw';
        confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 75%)`;
        
        // Random hình dạng
        if (Math.random() > 0.5) {
          confetti.style.borderRadius = '50%';
        } else {
          confetti.style.borderRadius = '0';
        }
        
        // Random kích thước
        const size = Math.random() * 10 + 5;
        confetti.style.width = `${size}px`;
        confetti.style.height = `${size}px`;
        
        // Thời gian rơi
        confetti.style.animationDuration = (2 + Math.random() * 3) + 's';
        
        document.body.appendChild(confetti);
        
        // Tự động xóa sau khi animation kết thúc
        setTimeout(() => {
          confetti.remove();
        }, 3000);
      }
    }
    
    // Xử lý sự kiện nút đồng ý
    document.getElementById('yesBtn').addEventListener('click', function() {
      createConfetti();
      
      // Thay đổi nội dung
      document.querySelector('h1').textContent = 'Em đã làm trái tim anh hạnh phúc!';
      document.querySelector('p').textContent = 'Cảm ơn em đã đồng ý, anh hứa sẽ làm em hạnh phúc mỗi ngày ❤️';
      
      // Ẩn nút
      document.getElementById('noBtn').style.display = 'none';
      this.textContent = 'Yêu em nhiều lắm!';
      
      // Phát nhạc
      const music = document.getElementById('bgMusic');
      music.play().catch(e => console.log("Auto-play was prevented: ", e));
      
      // Tăng số lượng trái tim
      setInterval(createHearts, 100);
    });
    
    // Xử lý sự kiện nút từ chối (di chuyển khi hover)
    document.getElementById('noBtn').addEventListener('mouseover', function() {
      const btn = this;
      const container = btn.parentElement;
      const containerRect = container.getBoundingClientRect();
      const btnRect = btn.getBoundingClientRect();
      
      // Tính toán vị trí mới không trùng với vị trí cũ
      let newX, newY;
      do {
        newX = Math.random() * (containerRect.width - btnRect.width);
        newY = Math.random() * (containerRect.height - btnRect.height);
      } while (
        Math.abs(newX - btn.offsetLeft) < btnRect.width && 
        Math.abs(newY - btn.offsetTop) < btnRect.height
      );
      
      btn.style.position = 'absolute';
      btn.style.left = newX + 'px';
      btn.style.top = newY + 'px';
    });
    
    // Bắt đầu tạo trái tim
    setInterval(createHearts, 300);
    
    // Hiệu ứng khi load trang
    window.addEventListener('load', function() {
      document.querySelector('.container').style.opacity = '1';
      document.querySelector('.container').style.transform = 'translateY(0)';
    });
    
    // Kiểm tra và yêu cầu tương tác trước khi phát nhạc
    document.body.addEventListener('click', function() {
      const music = document.getElementById('bgMusic');
      if (music.paused) {
        music.play().catch(e => console.log("Playback prevented: ", e));
      }
    }, { once: true });
  </script>
</body>
</html>
