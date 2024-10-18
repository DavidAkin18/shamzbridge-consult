<template>
    <div class="container">
      <footer class="footer">
        <div class="footer-text">
          <p>© ShamzBridge. All rights reserved.</p>
          <p>
            Office address: 4th Floor, Labour House, Central Business District, Abuja
          </p>
        </div>
        <div class="social-links">
          <a href="https://wa.me/123456789" target="_blank" aria-label="WhatsApp">
            <i class="ri-whatsapp-line"></i>
          </a>
          <a href="https://twitter.com/yourprofile" target="_blank" aria-label="Twitter">
            <i class="ri-twitter-line"></i>
          </a>
          <a href="tel:+123456789" aria-label="Phone">
            <i class="ri-phone-line"></i>
          </a>
          <a href="https://instagram.com/yourprofile" target="_blank" aria-label="Instagram">
            <i class="ri-instagram-line"></i>
          </a>
          <a href="https://linkedin.com/in/yourprofile" target="_blank" aria-label="LinkedIn">
            <i class="ri-linkedin-line"></i>
          </a>
          <a href="https://youtube.com/yourprofile" target="_blank" aria-label="YouTube">
            <i class="ri-youtube-line"></i>
          </a>
          <a href="https://x.com/yourprofile" target="_blank" aria-label="X (formerly Twitter)">
            <i class="ri-x-line"></i>
          </a>
        </div>
      </footer>
    </div>
  </template>
  
<script>
  export default {}
</script>
  
<style scoped>
html, body {
  height: 100%;
  margin: 0;
}
.container{
    background-color: #0056b3;
}
.footer {
  padding: 20px;
  color: white;
  text-align: center;
  flex-shrink: 0;
  
  border-top: 2px solid #f2f4f8;
}

.footer-text {
  margin-bottom: 10px; 
  text-align: left;
}

.social-links {
  margin-top: 10px;
}

.social-links a {
  margin: 0 10px;
  color: white;
  font-size: 1.5em;
  transition: color 0.3s ease, transform 0.3s ease; 
}

.social-links a:hover {
  color: #f2f4f9a0;
  transform: scale(1.2); 
}

/* For small screens (default layout: stacked) */
@media (max-width: 600px) {
  .footer {
    padding: 15px;
    font-size: 14px;
  }

  .social-links a {
    font-size: 1.2em;
  }
}

/* For larger screens (flex layout with space between) */
@media (min-width: 768px) {
  .footer {
    padding: 20px;
    font-size: 16px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 85%;
    margin: 0 auto;
  }

  .footer-text, .social-links {
    margin-bottom: 0;
  }

  .social-links a {
    font-size: 1.5em;
  }
}

</style>


  