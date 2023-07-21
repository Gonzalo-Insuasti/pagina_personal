<template>
    <div class="presentation-page">
      <nav class="navbar">
        <ul>
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#acerca">Acerca</a></li>
          <li @mouseenter="showContactList = true" @mouseleave="showContactList = false">
            <a href="/contact">Contacto</a>
          <ul v-show="showContactList" class="contact-list">
            <li><a href="https://www.facebook.com" target="_blank">Facebook</a></li>
            <li><a href="https://www.linkedin.com/in/gonzalo-insuasti-7a9103252" target="_blank">LinkedIn</a></li>
          </ul>
        </li>
        </ul>
      </nav>
      <section id="inicio" class="hero-section">
        <div class="hero-section">
        <img class="mimage" :src="imagesrc" :alt="imagealt">
        <div class="hero-text">
          <h1>Hola Mundo!</h1>
        </div>
      </div>
      </section>
     <section id="acerca" class="about-section">
        <div class="profile-section ">
        <div class="profile-image">
          <img class="mimage" :src="img2" :alt="imgalt">
          <p>{{ datos.nombre }}</p>
          <p>{{ datos.titulo }}</p>
          <p>{{ datos.correo }}</p>
        </div>
        <div class="profile-description,">
          <p>{{ presentacion }}</p>
        </div>
      </div>
     </section>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  let imagesrc = ref('/Ciudad.jpg'),
      imagealt = ref('Mi imagen');
  let img2 = ref('/Personal.jpg'),
    imgalt =ref('Mod');
  const datos = ref({
    nombre: 'Gonzalo Fabian Insuasi Tabla', 
    titulo: 'Licenciado en informatica', 
    correo: 'Gonzaloinsuasty21@gmail.com'
    } );
    const presentacion = `¡Hola! Soy un programador junior 
    con conocimientos de JavaScript, HTML y Vue.js. 
    Me apasiona el desarrollo web y estoy emocionado por seguir 
    aprendiendo y mejorando mis habilidades. Me considero una persona 
    trabajadora, responsable y comprometida con mi trabajo. Siempre estoy 
    buscando nuevos desafíos y oportunidades para crecer profesionalmente.`

    const showContactList = ref(false);
    
  </script>
  
  <style>
  .textoendiv{
  display: flex;
  flex-direction: column;
  align-items: center;
} 
  .presentation-page {
    text-align: center;
    padding-top: 50px;
    padding-left:0cm;
    width:  90vw;
  }
  
  nav {
    background-color: #333;
    padding: 1px 0;
  }
  .navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #333;
  padding: 10px 0;
  z-index: 1000; /*el z-index sea superior a otros elementos para mantenerla por encima */
}
  
  nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  
  nav li {
    display: inline-block;
    margin-right: 10px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }
  
  nav a {
    color: #fff;
    text-decoration: none;
    padding: 5px 10px;
    text-decoration: none;
    font-size: 2vw;
  }
  
  .hero-section {
    position: relative;
    margin-top: 10px;
  }
  
  .hero-section img {
    width: 100%;
    max-height: 100%;
    object-fit: cover;
  }
  
  .hero-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  
  .hero-text h1 {
    color: #fff;
    font-size:  4vw;
    text-shadow: 2px 1px 2px black;
    
  }
  
  .profile-section {
    display: flex;
    justify-content: space-between;
    margin-top: 40px;
    font-size: 2.5vw;
  
  } 
  .profile-image p {
    text-align: left;
    font-size: 1.5vw;
  }
  .profile-image img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    margin-right: 50px;
  }
  
  .profile-description {
    max-width: 60%;
    text-align: left;
  }
  
  .profile-description p {
    font-size: 18px;
    line-height: 1.6;
  }

  .contact-dropdown {
  list-style: none;
  margin: 5px 0;
  position: relative;
  top: 100%;
  background-color: #fff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.2);
  display: none;
}
/* Mostrar el menú desplegable cuando el estado showContactDropdown es true */
.contact-dropdown.show {
  display: block;
}  
  </style>
  