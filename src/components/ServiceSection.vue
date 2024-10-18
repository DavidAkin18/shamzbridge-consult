<template>
    <div class="container">
        <section id="services" class="services-section">
            <h2>Our Services</h2>
            <div class="service-cards">
                <div class="service-card">
                    <div class="icon">
                        <i class="ri-hammer-line"></i>
                    </div>
                    <h3>Programs/Projects Management</h3>
                    <p>Partner with us for seamless project execution.</p>
                </div>
                <div class="service-card">
                    <div class="icon">
                        <i class="ri-line-chart-line"></i>
                    </div>
                    <h3>Capacity Building</h3>
                    <p>Nurture talent and skills with our capacity building services.</p>
                </div>
                <div class="service-card">
                    <div class="icon">
                        <i class="ri-team-fill"></i>
                    </div>
                    <h3>Consultancy Services</h3>
                    <p>Elevate your strategy with our consultancy services.</p>
                </div>
                <div class="service-card">
                    <div class="icon">
                        <i class="ri-mic-2-fill"></i>
                    </div>
                    <h3>Event Host/Management</h3>
                    <p>Let us handle the details while you enjoy the moment.</p>
                </div>
                <div class="service-card">
                    <div class="icon">
                        <i class="ri-shake-hands-line"></i>
                    </div>
                    <h3>Community Development</h3>
                    <p>Championing development where it matters most.</p>
                </div>
                <div class="service-card">
                    <div class="icon">
                        <i class="ri-video-on-fill"></i>
                    </div>
                    <h3>Content Development</h3>
                    <p>Unleash your creativity and transform ideas into impactful stories.</p>
                </div>
            </div>
            </section>
    </div>
</template>
  
<script>
export default {}
</script>
  
<style scoped>
.container{
    background-color: #f2f4f8; 
}
.services-section {
  padding: 20px;
  text-align: center;
}

h2 {
  font-size: 2em;
  color: #0056b3; 
  margin-bottom: 20px; 
}

/* Flexbox for mobile view (one column) */
.service-cards {
  display: flex;
  flex-direction: column; 
  gap: 20px; 
  line-height: 30px;
}

.service-card {
  background-color: #0056b3; 
  color: white; 
  padding: 20px 10px;
  border-radius: 8px;
  transition: transform 0.3s ease, background-color 0.3s ease, box-shadow 0.3s ease; 
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); 
}

.service-card:hover {
  transform: translateY(-10px); 
  background-color: #004494;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2); 
}

.icon {
  background: #f2f4f8;
  border-radius: 100%;
  padding: 30px;
  width: 30%;
  text-align: center;
  margin: 0 auto;
}

i {
  color: #004494;
  text-align: center;
  font-size: 1.5em;
}

/* For medium screens and up (min-width: 768px) */
@media (min-width: 768px) {
  .service-cards {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px; 
  }
}

/* For large screens and up (min-width: 1024px) */
@media (min-width: 1024px) {
  .services-section {
    width: 85%;
    margin: 0 auto;
  }

  .service-cards {
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }

  .service-card {
    padding: 30px 10px;
    width: 100%;
  }
}
</style>
