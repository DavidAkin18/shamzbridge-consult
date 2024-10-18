<template>
    <section id="about" class="about-section">
      <h2>Our Vision and Mission</h2>
      <p>
        Redefining industry standards through consultation, our innovative approach 
        integrates cutting-edge technology with expert insights, driving transformative 
        change and setting new benchmarks for excellence.
      </p>
      <div class="contain-mission">
        <div class="mission-and-vision">
          <h3 class="mission-head">Vision</h3>
          <p class="mission-body">
            To become a premier organization dedicated to enhancing both personal and 
            professional capacities of individuals and businesses, fostering efficiency, 
            heightened productivity, and innovation.
          </p>
        </div>
        <div class="mission-and-vision">
          <h3 class="mission-head">Mission</h3>
          <p  class="mission-body">
            Our mission is to cultivate an empowering atmosphere for skill acquisition 
            and capacity enhancement that heralds holistic growth and development for 
            individuals and organizations.
          </p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {}
  </script>
  
  <style scoped>
  .about-section {
    padding: 20px;
    background-color: #f2f4f8; 
    text-align: center;
  }
  
  h2 {
    font-size: 1.5em;
    color: #0056b3;
    margin: 0 0 10px; 
  }
  
  p {
    font-size: 1em;
    color: #777; 
    text-align: center;
    line-height: 30px;
    margin: 0 auto;
  }
  
  .mission-head {
    color: #000;
    margin: 0 0 10px; 
  }
  
  .contain-mission {
    display: flex;
    flex-direction: column; 
    gap: 20px;
    padding-top: 40px;
  }
  
  .mission-and-vision {
    background: #fff;
    padding: 20px;
    color: #000;
    border-radius: 8px; 
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s, box-shadow 0.3s; 
  }
  .mission-body{
    color: #777;
  }
  /* Hover effect */
  .mission-and-vision:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); 
  }
  
  /* Medium screens and up (min-width: 768px) */
  @media (min-width: 768px) {
    .about-section {
      /* padding: 60px; */
    }
  
    h2 {
      font-size: 2em;
    }
  
    p {
      font-size: 1.1em;
      width: 80%;
    }
  }
  
  /* Large screens and up (min-width: 1024px) */
  @media (min-width: 1024px) {
    .about-section {
      padding: 80px;
    }
  
    h2 {
      font-size: 2.5em;
    }
    .mission-body{
        width: 100%;
    }
    p {
      font-size: 1.2em;
      width: 60%;
    }
    .contain-mission {
      flex-direction: row; 
      gap: 10px;
      justify-content: space-around; 
    }
    .mission-and-vision {
      flex: 1;
      margin: 0 10px; 
      padding: 30px; 
    }
  }
  </style>
  