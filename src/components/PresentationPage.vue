<template>
    <link rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
  integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw=="
  crossorigin="anonymous"
  referrerpolicy="no-referrer" />
    <div class="presentation-page">
      <nav class="navbar">
        <ul>
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#acerca">Acerca</a></li>

          <div class="dropdown"  >
                <button class="btnright" >
                  <span>CONTACTO</span>
                </button>
                <div class="dropdown-options">
                  <li><a href="https://www.linkedin.com/in/gonzalo-insuasti-7a9103252" target="_blank">Linkedin <i class="fa-brands fa-linkedin fa-fade"></i></a></li>
                  <li><a href="https://instagram.com/gonzalo_xz?igshid=NGExMmI2YTkyZg==" target="_blank">Instagram <i class="fa-brands fa-instagram fa-fade"></i></a></li>
                </div>
              </div>

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
          <a :href="doc" download="DocCV.pdf">
          <button class="btn">Descargar CV</button>
          </a>
        </div>
        <div class="profile-description,">
          <p>{{ presentacion }}</p>
        </div>
      </div>
     </section>

     <section>
      <h1>EDUCACIÓN Y TITULACIÓN</h1>
      <br>
      <div style="text-align: left;">
        <ul>
          <li><b>{{ datos.titulo }}</b> <ul>
            <li>Universidad de Nariño, Pasto</li>
            <li>Agosto 2017 - Junio 2023</li>
          </ul></li>
          <p>Durante mi licenciatura en Informática, adquirí una formación en programación,
            bases de datos, algoritmos y desarrollo de software</p>
          <li>Cursos programación Platzi:<ul>
            <li>Basico JavaScript</li>
            <li>Asincronismo JavaScript</li>
            <li>Closures y Scope JavaScript</li>
            <li>Vue js</li>
          </ul></li>
          <li>Git y GitHub</li>
          <br>
          <p>En los cursos que estoy realizando actualmente espero seguir aprendiendo mucho mas sobre programación
            fron end y asi apliar mi conocimiento con mas herramientas.
            <br>
            <br>
            En estos cursos de programación, he ampliado mis conocimientos en áreas específicas
            de desarrollo front end y he aprendido a utilizar herramientas y tecnologías relevantes para el campo.
            Estos cursos me han proporcionado una base para abordar proyectos y me han ayudado
            a mantenerme actualizado con las últimas tendencias en programación.</p>
        </ul>
      </div>
     </section>
     <br>
     <br>

    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  let imagesrc = ref('/Ciudad.jpg'),
      imagealt = ref('Mi imagen');
  let img2 = ref('/Personal.jpg'),
    imgalt =ref('Mod');
  let doc = ref('/DocCV.pdf');
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
    .btnright {
    border: 0;
    background-image: linear-gradient(
      150deg,
      #9500ff,
      #09f,
      #00DDFF
    );
    border-radius: 8PX;
    color: #fff;
    display: flex;
    font-size: 1.3vw;
    padding: 4px;
    cursor: pointer;
    transition: .3s ;

  }
  button span {
    background-color: #333;
    padding: 16px 24px;
    border-radius: 6px;
    transition: .3s;
  }
  button:hover span {
    background: none;
  }
  button:active{
    transform: scale(0.9);
  }

.btn {
    background-color: #007bff;
    color: #fff;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 4px;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  .dropdown {
  display: inline-block;
  position: relative;
}


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
    text-align: right;
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
    margin-right: 20px;
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
    font-size: 1.2vw;
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
  .dropdown-options {
  display: none;
  position: absolute;
  overflow: auto;
  text-align: left;
}
  .dropdown:hover .dropdown-options {
  display: block;
}
  </style>
  