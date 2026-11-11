# welcome-shakti-hotel-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title id="pageTitle">Hotel</title>

<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: Arial, sans-serif;
    background: #fff8f0;
    color: #222;
  }

  .banner {
    position: relative;
    height: 70vh;
    min-height: 420px;
    overflow: hidden;
  }

  /* R K BY DANCE LOGO */
  .brand-logo {
    position: absolute;
    top: 15px;
    right: 15px;
    z-index: 10;
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 7px 10px;
    background: rgba(0,0,0,0.78);
    border: 1px solid #d6ad52;
    border-radius: 8px;
    color: #e8c36b;
  }

  .brand-logo svg {
    width: 30px;
    height: 30px;
  }

  .brand-name {
    font-size: 11px;
    font-weight: bold;
    white-space: nowrap;
  }

  .brand-name small {
    display: block;
    font-size: 7px;
    letter-spacing: 1px;
    margin-top: 3px;
    color: #fff;
  }

  .slider {
    position: absolute;
    left: 0;
    width: 100%;
    height: 50%;
    overflow: hidden;
  }

  .slider.rooms { top: 0; }
  .slider.food { top: 50%; }

  .slider img {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0;
    transition: opacity 1s;
  }

  .slider img.active { opacity: 1; }

  .label {
    position: absolute;
    left: 12px;
    bottom: 10px;
    z-index: 3;
    background: rgba(0,0,0,0.55);
    color: #fff;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 13px;
  }

  .overlay {
    position: absolute;
    inset: 0;
    z-index: 2;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #fff;
    background: rgba(0,0,0,0.35);
    padding: 16px;
  }

  .overlay h1 {
    font-size: 2.2rem;
    text-shadow: 0 2px 8px #000;
  }

  .overlay p {
    margin-top: 8px;
    font-size: 1.05rem;
    text-shadow: 0 2px 6px #000;
  }

  .buttons {
    display: flex;
    gap: 14px;
    justify-content: center;
    padding: 18px 12px;
    flex-wrap: wrap;
  }

  .btn {
    text-decoration: none;
    padding: 14px 28px;
    border-radius: 30px;
    font-weight: bold;
    font-size: 1rem;
    color: #fff;
    position: relative;
    overflow: hidden;
    display: inline-block;
  }

  .btn.call { background: #1faa3f; }
  .btn.book { background: #ff8c1a; }

  .btn.book::after {
    content: '';
    position: absolute;
    top: 0;
    left: -80%;
    width: 50%;
    height: 100%;
    background: linear-gradient(
      120deg,
      transparent,
      rgba(255,255,255,0.7),
      transparent
    );
    animation: shine 2.5s infinite;
  }

  @keyframes shine {
    to { left: 130%; }
  }

  .booking {
    max-width: 480px;
    margin: 10px auto 30px;
    background: #fff;
    padding: 20px;
    border-radius: 14px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.12);
  }

  .booking h2 {
    margin-bottom: 12px;
    text-align: center;
  }

  .booking input,
  .booking select {
    width: 100%;
    padding: 12px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 1rem;
  }

  .booking button {
    width: 100%;
    padding: 14px;
    border: none;
    border-radius: 8px;
    background: #25d366;
    color: #fff;
    font-size: 1.05rem;
    font-weight: bold;
    cursor: pointer;
  }

  .menu {
    max-width: 480px;
    margin: 10px auto 40px;
    padding: 0 12px;
  }

  .menu h2 {
    text-align: center;
    margin-bottom: 14px;
  }

  .menu-box {
    background: #fff;
    border-radius: 14px;
    padding: 16px 18px;
    margin-bottom: 14px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.12);
  }

  .menu-box h3 {
    color: #ff8c1a;
    margin-bottom: 10px;
    border-bottom: 2px solid #ffe0bf;
    padding-bottom: 6px;
  }

  .dish {
    display: flex;
    justify-content: space-between;
    padding: 7px 0;
    border-bottom: 1px dashed #e3e3e3;
    font-size: 1rem;
  }

  .dish:last-child { border-bottom: none; }

  .dish .price {
    font-weight: bold;
    color: #1faa3f;
  }

  @media(max-width: 400px) {
    .brand-logo {
      top: 8px;
      right: 8px;
      padding: 5px 7px;
    }

    .brand-logo svg {
      width: 24px;
      height: 24px;
    }

    .brand-name { font-size: 9px; }

    .brand-name small { font-size: 6px; }
  }
</style>
</head>

<body>

<div class="banner">

  <!-- R K BY DANCE LOGO -->
  <div class="brand-logo">

    <svg viewBox="0 0 100 100"
         xmlns="http://www.w3.org/2000/svg">

      <defs>
        <linearGradient id="gold" x1="0" y1="0" x2="1" y2="1">
          <stop offset="0%" stop-color="#fff0b0"/>
          <stop offset="50%" stop-color="#d6aa45"/>
          <stop offset="100%" stop-color="#8d6420"/>
        </linearGradient>
      </defs>

      <circle cx="50" cy="50" r="46"
        fill="none"
        stroke="url(#gold)"
        stroke-width="5"/>

      <text x="50" y="62"
        text-anchor="middle"
        font-size="38"
        font-weight="bold"
        fill="url(#gold)">RK</text>

    </svg>

    <div class="brand-name">
      R K by Dance
      <small>PTEL PRIVATE LIMITED</small>
    </div>

  </div>

  <div class="slider rooms" id="roomsSlider">
    <span class="label">Our Rooms</span>
  </div>

  <div class="slider food" id="foodSlider">
    <span class="label">Our Food</span>
  </div>

  <div class="overlay">
    <h1 id="hotelNameText"></h1>
    <p id="taglineText"></p>
  </div>

</div>

<div class="buttons">
  <a class="btn call" id="callBtn" href="#">Call Now</a>
  <a class="btn book" href="#booking">Book Your Room</a>
</div>

<div class="booking" id="booking">

  <h2>Book on WhatsApp</h2>

  <input type="text" id="guestName" placeholder="Your name">

  <input type="date" id="checkIn">

  <input type="date" id="checkOut">

  <select id="guests">
    <option>1 Guest</option>
    <option>2 Guests</option>
    <option>3 Guests</option>
    <option>4 Guests</option>
    <option>5+ Guests</option>
  </select>

  <button onclick="sendWhatsApp()">
    Send Booking on WhatsApp
  </button>

</div>

<div class="menu" id="menuSection">
  <h2>Our Menu</h2>
</div>

<script>

/* HOTEL SETTINGS */

const HOTEL_NAME = "Shakti Hotel and Guest House";

const TAGLINE =
"On the Dwarka - Somnath - Veraval Highway";

const PHONE_NUMBER = "91XXXXXXXXXX";

const WHATSAPP_NUMBER = "91XXXXXXXXXX";

const ROOM_IMAGES = [
  "ROOM PHOTO 1 LINK"https://maps.app.goo.gl/ipgJ6DZKTQbD9gUp7,
  "ROOM PHOTO 2 LINK"https://maps.app.goo.gl/6AJofQBRDiorz2Nz6,
  "ROOM PHOTO 3 LINK"https://maps.app.goo.gl/bUus4956pV4iBx4g9,
  "ROOM PHOTO 4 LINK"https://maps.app.goo.gl/LUrhQkpUDjdTX6dh6,
  "ROOM PHOTO 5 LINK"https://maps.app.goo.gl/HjUjCaiHf4P7WXfV7,
  "ROOM PHOTO 6 LINKh"https://maps.app.goo.gl/qrE2fcLfi4A3MdsY9,
  "ROOM PHOTO 7 LINk"https://maps.app.goo.gl/bUus4956pV4iBx4g9,
];

const FOOD_IMAGES = [
  "FOOD PHOTO 1 LINK""https://maps.app.goo.gl/PcV2TALFpcUfqMjTA,,
  "FOOD PHOTO 2 LINK"https://maps.app.goo.gl/ZLR93f9NyGwh9tD5Ahttps,
  "FOOD PHOTO 3 LINK"https://maps.app.goo.gl/AVyqbEySBhWshd3U6,
  "FOOD PHOTO 4 LINK"https://maps.app.goo.gl/AVyqbEySBhWshd3U6,
  "FOOD PHOTO 5 LINK"https://maps.app.goo.gl/vvzkh6r9B7eD5L4m9,
  "FOOD PHOTO 6 LINK"https://maps.app.goo.gl/EWuQZz4rLegiFDaq8,
  "FOOD PHOTO 7 LINK"ttps://maps.app.goo.gl/hFLyT79arcoSt9op7,
];

const SLIDE_SECONDS = 3;

const MENU = [
  {
    category: "Punjabi",
    dishes: [
      { name: "Paneer Butter Masala", price: 220 },
      { name: "Dal Tadka", price: 140 },
      { name: "Butter Naan", price: 40 }
    ]
  },
  {
    category: "Chinese",
    dishes: [
      { name: "Veg Hakka Noodles", price: 150 },
      { name: "Veg Manchurian", price: 160 },
      { name: "Fried Rice", price: 140 }
    ]
  },
  {https://maps.app.goo.gl/bUus4956pV4iBx4g9
    category: "Gujarati Thali",
    dishes: [
      { name: "Full Thali", price: 250 },
      { name: "Mini Thali", price: 160 }
    ]
  }
];

/* WEBSITE FUNCTIONALITY */

document.getElementById('pageTitle').textContent = HOTEL_NAME;

document.getElementById('hotelNameText').textContent = HOTEL_NAME;

document.getElementById('taglineText').textContent = TAGLINE;

document.getElementById('callBtn').href = 'tel:+' + PHONE_NUMBER;


function startSlider(containerId, images) {

  const box = document.getElementById(containerId);

  images.forEach(function (src, i) {

    const img = document.createElement('img');

    img.src = src;

    if (i === 0) {
      img.classList.add('active');
    }

    box.appendChild(img);

  });

  const imgs = box.querySelectorAll('img');

  let current = 0;

  if (imgs.length > 1) {

    setInterval(function () {

      imgs[current].classList.remove('active');

      current = (current + 1) % imgs.length;

      imgs[current].classList.add('active');

    }, SLIDE_SECONDS * 1000);

  }

}


startSlider('roomsSlider', ROOM_IMAGES);

startSlider('foodSlider', FOOD_IMAGES);


function buildMenu() {

  const section = document.getElementById('menuSection');

  MENU.forEach(function (group) {

    const box = document.createElement('div');

    box.className = 'menu-box';

    const title = document.createElement('h3');

    title.textContent = group.category;

    box.appendChild(title);

    group.dishes.forEach(function (d) {

      const row = document.createElement('div');

      row.className = 'dish';

      const n = document.createElement('span');

      n.textContent = d.name;

      const p = document.createElement('span');

      p.className = 'price';

      p.textContent = '₹' + d.price;

      row.appendChild(n);

      row.appendChild(p);

      box.appendChild(row);

    });

    section.appendChild(box);

  });

}


buildMenu();


function sendWhatsApp() {

  const name = document.getElementById('guestName').value;

  const inDate = document.getElementById('checkIn').value;

  const outDate = document.getElementById('checkOut').value;

  const guests = document.getElementById('guests').value;

  const msg =
    'Hello, I want to book a room at ' + HOTEL_NAME +
    '.\nName: ' + name +
    '\nCheck-in: ' + inDate +
    '\nCheck-out: ' + outDate +
    '\nGuests: ' + guests;

  window.open(
    'https://wa.me/' + WHATSAPP_NUMBER +
    '?text=' + encodeURIComponent(msg),
    '_blank'
  );

}

</script>

</body>
</html>
