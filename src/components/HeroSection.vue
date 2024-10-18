<template>
   <div class="container">
    <section id="hero" class="hero-section">
        <!-- <h1>Welcome to Shamzbridge Consult</h1> -->
        <h1>
            Build an Organization of High Repute,Immerse yourself 
            in <span class="animated-skill">{{ currentSkill }}</span> for Self Sustenance
        </h1>
        <button class="cta-btn">Learn More</button>
    </section>
   </div>
 </template>
 
 <script>
 export default {
    data() {
    return {
      skills: [
        'Transferable skills',
        'In-Demand skills',
        'Marketable skill set',
        'Transferable skills'
      ],
      currentSkill: '',
      skillIndex: 0
    };
  },
  mounted() {
    this.currentSkill = this.skills[this.skillIndex];
    this.startSkillAnimation();
  },
  methods: {
    startSkillAnimation() {
      setInterval(() => {
        this.skillIndex = (this.skillIndex + 1) % this.skills.length;
        this.currentSkill = this.skills[this.skillIndex];
      }, 3000); // Change skill every 3 seconds
    }
  }

 }
 </script>
 
 <style scoped>
 .container{
    width: 100%;
    background-color: #fff;
    padding: 4rem 0 ;
    padding-top: 7rem;
    
    
 }
.hero-section {
  text-align: center;
  margin: 0 auto;
  color: #0056b3;
}

h1 {
  margin: 0; 
}

.animated-skill {
  display: inline-block;
  opacity: 0;
  animation: fadeIn 0.2s forwards; 
  color: #000;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
    transform: translateY(-10px); 
  }
  100% {
    opacity: 1;
    transform: translateY(0); 
  }
}

.cta-btn {
  background-color: #0056b3;
  color: #fff; 
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: bold;
  border: none;
  transition: background-color 0.3s, color 0.3s; 
}

.cta-btn:hover {
  background-color: #004494;
  color: #e2e2e2; 
}

/* Medium screens and up (min-width: 768px) */
@media (min-width: 768px) {
  .hero-section {
    padding: 4rem;
    padding-top: 2rem;
  }
  
  h1 {
    font-size: 2em;
    line-height: 45px;
    margin-bottom: 20px;
  }
  
  .cta-btn {
    padding: 12px 25px;
    font-size: 1.1em;
  }
}

/* Large screens and up (min-width: 1024px) */
@media (min-width: 1024px) {
    .hero-section {
        width: 80%;
        margin: 0 auto;
    }
  
  h1 {
    font-size: 2.5em;
    padding: 10px 12px;
  }

  p {
    font-size: 1.25em;
  }

  .cta-btn {
    padding: 15px 30px;
    font-size: 1.2em;
  }
}


 </style>
 