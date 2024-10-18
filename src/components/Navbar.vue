<template>
    <nav class="navbar">
      <div class="nav-container">
        <a href="#" class="logo">
            <img src="https://res.cloudinary.com/def9quyti/image/upload/v1729250703/logo_odskby.png" 
            alt="logo" class="logo-img" >
        </a>
        <!-- Menu icon for small screens -->
        <button class="menu-icon" @click="toggleMenu" v-if="isMobile">
          <i class="ri-menu-line"></i>
        </button>
        <!-- Navigation items -->
        <ul :class="{'nav-items': true, 'mobile-open': isMenuOpen}">
          <li><a href="#about">About Us</a></li>
          <li><a href="#events">Events</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#contact">Testimonials</a></li>
          <li><a href="#careers">Careers</a></li>
        </ul>
      </div>
      <div v-if="isMenuOpen && isMobile" class="backdrop" @click="closeMenu"></div>
      
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isMenuOpen: false,
        isMobile: window.innerWidth <= 768
      };
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen;
      },
      closeMenu() {
        this.isMenuOpen = false;
      },
      handleResize() {
        this.isMobile = window.innerWidth <= 768;
        if (!this.isMobile) {
          this.isMenuOpen = false;
        }
      }
    },
    mounted() {
      window.addEventListener('resize', this.handleResize);
    },
    beforeDestroy() {
      window.removeEventListener('resize', this.handleResize);
    }
  };
  </script>
  
  <style scoped>
  /* Navbar styles */
  .navbar {
      position: fixed;
      width: 100%;
      z-index: 99;
      background-color: #ffffff; 
      padding: 20px 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 2px solid #ffffff;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .nav-container {
      display: flex;
      justify-content: space-between;
      width: 100%;
      margin: 0 auto;
      align-items: center;
  }
  
  /* Navigation items */
  .nav-items {
      list-style: none;
      display: flex;
      gap: 20px;
      padding: 5px 20px;
      transition: transform 0.3s ease;
  }
  
  /* Navigation links */
  .nav-items li a {
      color: #0056b3;
      font-weight: bold;
      text-decoration: none;
      transition: color 0.3s ease;
  }
  
  .nav-items li a:hover {
      color: #004494; 
  }
  
  /* Logo styles */
  .logo-img {
      width: 120px; 
      height: auto;
      max-height: 50px; 
  }
  
  /* Menu icon styles */
  .menu-icon {
      display: none;
      background: none;
      border: none;
      font-size: 24px;
      color: #0056b3; 
  }
  
  /* Backdrop styles */
  .backdrop {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1;
  }
  
  /* Media Query for screens 768px and below */
  @media (max-width: 768px) {
      .menu-icon {
          display: block;
          cursor: pointer;
          z-index: 3;
      }
  
      .nav-items {
          position: fixed;
          top: 0;
          right: 0;
          width: 250px;
          height: 100%;
          background-color: #ffffff; 
          flex-direction: column;
          padding-top: 60px;
          gap: 15px;
          transform: translateX(100%);
          z-index: 2;
          box-shadow: -2px 0 5px rgba(0, 0, 0, 0.3);
      }
  
      .mobile-open {
          transform: translateX(0);
      }
  
      /* Mobile navigation link styles */
      .nav-items li a {
          color: #0056b3; 
          font-weight: bold;
      }
  
      .nav-items li a:hover {
          color: #004494; 
      }
  }
  
  /* Media Query for screens above 768px */
  @media (min-width: 769px) {
    .nav-container{
        width: 85%;
    }
    .menu-icon {
        display: none;
    }

    .nav-items {
        flex-direction: row;
        position: static;
        transform: none;
    }

    .nav-items li {
        margin: 0;
    }
    .logo-img {
        width: 200px;        
    }
  }
  </style>
  
  