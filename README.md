<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8" />
  <title>Portofoliu - Corondan Flavius</title>
  <style>
    /* Global box-sizing */
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      padding: 0;
      font-family: sans-serif;
      background-color: #17082c;
      color: #fff;
      overflow-x: auto;
      overflow-y: auto;
    }
    .page-wrapper {
      width: 100%;
      max-width: 1600px;
      margin: 0 auto;
    }
      
    header {
      padding: 30px 40px;
      background-color: #111;
    }
    .header-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 100%;
      gap: 80px;
      min-width: 900px;
      margin: 0;
    }
    .text-section {
      white-space: nowrap;
    }
    .text-section h1 {
      font-size: 1.8rem;
      margin: -15px 0 5px 0;
    }
    
    .project-description h2 {
       font-size: 1.3rem;
      margin: 0 25px;
      margin-top: 40px;
      opacity: 0.5;
      transition: opacity 0.5s ease-out;

    }

    /* Clasa pentru proiectul activ */
    .project.project-active .project-description h2 {
      opacity: 1;
      transition: opacity 1.5s ease;
    }
    
    .text-section p {
      font-size: 1.5rem;
      margin: 40px 10px 0;
      font-weight: bold;
    }
    .profile-gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      margin-left: 140px;
    }
    .profile-gallery img {
      width: 80px;
      height: 100px;
      object-fit: cover;
      border-radius: 20px;
      border: 5px solid #4a3160;
      transition: transform 0.3s ease;
      cursor: zoom-in;
    }
    .profile-gallery img:hover {
      transform: scale(1.05);
    }
    .section {
      padding: 10px;
      margin: 10px;
    }
    .gallery {
      display: flex;
      flex-direction: column;
      gap: 40px;
    }
    .image-box {
      position: relative;
      min-height: 20px;
      width: 100%;
      background-color: #4a3160;
      padding:20px;
      border-radius: 10px;
      display: flex;
      flex-direction: row; /* Schimbat pentru a alinia imaginea și textul pe orizontală */
      gap: 10px;
   

      
  overflow: hidden;
  max-height: 120px;
  opacity: 0.6; /* 80% transparent */
  transition: max-height 1s ease; /* 0.5 secunde pentru retragere */
    }

    .image-box:hover {
      /* Pentru a arăta efectul de hover și a lansa animația textului */
      max-height: 1000px;
      opacity: 1;
      }

  /* 1. NORMAL: ascund prompt-ul complet */
.image-box .prompt {
  opacity: 0;
  transition: opacity 0.5s ease-out;
}

/* 2. NORMAL: celelalte elemente (imagini, titlu etc) le poți lăsa la 0.6 */
.image-box img,
.image-box .project-description h2,
.image-box img.main-img,
.image-box .arrow,
.image-box .plansa-redusa {
  opacity: 0.6;
  transition: opacity 0.5s ease-out;
}

/* 3. HOVER: arăt prompt-ul și celelalte elemente full opacity */
.image-box:hover .prompt {
  opacity: 1;
}
.image-box:hover img,
.image-box:hover .project-description h2,
.image-box:hover img.main-img,
.image-box:hover .arrow,
.image-box:hover .plansa-redusa {
  opacity: 1;
  transition: opacity 2s ease;
}


 
    .image-box.open {
  /* Când este deschis, se extinde mai lent */
  max-height: 1000px;  /* O valoare suficient de mare pentru a afișa tot conținutul */
  opacity: 1;  
  transition: max-height 2s ease; /* 1.5 secunde pentru deschidere */
}



    .image-row {
      display: flex;
      gap: 20px;
      align-items: flex-start;
      flex-wrap: wrap;
    }
    .image-box img.main-img {
      width: 450px;
      max-width: 100%;
      display: block;
      border-radius: 5px;
      object-fit: cover;
      transition: transform 0.3s ease;
    }
    .plansa-redusa {
      width: 445px !important;
    }
    .coperta-redusa {
      width: 445px !important;
      height: auto;
    }
    .sub-gallery {
      padding-left: 0px;
      display: flex;
      gap: 15px;
      overflow-x: hidden;
      scroll-behavior: smooth;
      width: 800px;
      -ms-overflow-style: none;
      scrollbar-width: none;
      margin-left: 30px;
    }

    .box-adjust .sub-gallery {
      padding-left: 0px;
      display: flex;
      gap: 15px;
      overflow-x: hidden;
      scroll-behavior: smooth;
      width:1100px;
      -ms-overflow-style: none;
      scrollbar-width: none;
      margin-left: 30px;
    }


    
    .sub-gallery::-webkit-scrollbar {
      display: none;
    }
    
    .sub-gallery img {
      height: 125px;
      object-fit: cover;
      transition: transform 0.3s ease;
      cursor: pointer;
      margin-right: 10px;
      border-radius: 10px;
    }



    .sub-gallery-large img {
  height: 170px;
}

.box-adjust .sub-gallery img {
  height: 170px;
}


    .image-box img.main-img:hover,
    .sub-gallery img:hover {
      transform: scale(1.05);
    }

    .prompt {
  width: 250px; /* Lățimea fixă dorită */
  white-space: normal; /* Permite textului să se împartă pe mai multe rânduri */
  text-align: justify; /* Aliniere la dreapta */
  font-size: 0.75rem;
  color: white;
  padding: 5px;
  margin-left: auto;
  margin-top: 50px;
  overflow-wrap: break-word;
  position: relative;
  overflow: visible;
  border-right: 2px solid transparent;
  
}

.box-adjust .prompt {
   width: 250px; /* Lățimea fixă dorită */
  white-space: normal; /* Permite textului să se împartă pe mai multe rânduri */
  text-align: justify; /* Aliniere la dreapta */
  font-size: 0.75rem;
  color: white;
  padding: 5px;
  margin-left: auto;
  margin-top: 30px;
  overflow-wrap: break-word;
  position: relative;
  overflow: visible;
  border-right: 2px solid transparent;
  
}
 /* Fiecare literă este într-un span cu clasa .letter */
    .prompt .letter {
  display: inline-block;
  vertical-align: baseline;
  line-height: inherit;
  white-space: pre;
  opacity: 0;
  transform: translateY(0.3em);
  will-change: opacity, transform;
  animation-fill-mode: forwards;
  transform: translateY(0.01em);
  /* elimina orice altă animație default */
  animation: none;
    }



    /* La hover pe containerul părinte (image-box) declanșăm animația */
   .image-box:hover .prompt .letter {
  animation-name: typewriterLetter;
  animation-duration: 0.1s;
  animation-timing-function: steps(1,end);
  animation-fill-mode: forwards;
}


.animated-word {
  /* Proprietatea white-space: nowrap este deja setată inline, dar poți seta și aici pentru siguranță */
  white-space: nowrap;
}





   @keyframes typewriterLetter {
  from { 
    opacity: 0; 
  }
  to { 
    opacity: 1; 
  }
}





.static-text {
  color: rgb(255, 255, 255); /* Asigură că textul static va avea culoare albă */
}
  
    .sub-gallery-wrapper {
      position: relative;
      display: flex;
      align-items: center;
      width: 650px;
      overflow-x: visible;
      margin-top: 50px;
    }

    .box-adjust .sub-gallery-wrapper {
   position: relative;
      display: flex;
      align-items: center;
      width:1100px;
      overflow-x: visible;
      margin-top: 5px;
    }

    .arrow {
      position: absolute;
      width: 30px;
      height: 80px;
      background: rgba(255, 255, 255, 0.655);
      cursor: pointer;
      top: 50%;
      transform: translateY(-50%);
      z-index: 10;
      clip-path: polygon(0% 0%, 100% 50%, 0% 100%, 0% 50%);
    }
    .arrow.arrow-left {
      transform: translateY(-50%) scaleX(-1);
      left: -5px;
    }
    .arrow.arrow-right {
      right: -36px;
    }

    

    #lightbox {
      position: fixed;
      display: none;
      justify-content: center;
      align-items: center;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: rgba(0, 0, 0, 0.85);
      z-index: 9999;
      padding: 20px;
      overflow: auto;
    }
    #lightbox img {
      object-fit: contain;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(255,255,255,0.3);
      transition: opacity 0.3s ease-in-out;
      display: block;
      margin: auto;
      width: 95vw;
      max-height: 95vh;
    }
    #lightbox:after {
      content: "✖";
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: white;
      cursor: pointer;
    }



    .expand-indicator {
  position: absolute;
  top: 0px;
  left: 50%;
  font-size: 3rem;
  color: #ffffff;
  opacity: 0.6;
  transition: transform 0.3s ease, opacity 0.3s ease;
  pointer-events: none;
   transform: translateX(-100%) scaleX(2); /* întins orizontal */
}


.image-box:hover .expand-indicator {
  opacity: 0;
   }





   .contact-info {
  display: flex;
  align-items: center;
  gap: 25px;
  margin-left: auto;
  margin-right: 15px;
}

.contact-info img {
  width: 24px;
  height: 24px;
  filter: invert(1); /* pentru icon alb pe fundal închis */
}

.contact-text {
  font-size: 0.9rem;
  color: #fff;
  text-decoration: none;
  opacity: 0.8;
  transition: opacity 0.3s;
}

.contact-text:hover {
  opacity: 1;
}




  </style>
</head>
<body>
  <div class="page-wrapper">
    <header>
      <div class="header-content">
        <div class="text-section">
          <h1>Corondan Flavius</h1>
          <p>Portofoliu Personal</p>
        </div>
        <div class="profile-gallery">
          <img src="Drona.png" alt="Poză 1" />
          <img src="Statietotala.png" alt="Poză 2" />
          <img src="deseniubita.jpg" alt="Poză 3" />
          <img src="Faro2.jpg" alt="Poză 4" />
        </div>
     


       <div class="contact-info">
      <a href="https://www.linkedin.com/in/flavius-corondan-920600331/" target="_blank" class="contact-icon">
        <img src="Linkedin.png" alt="LinkedIn" />
      </a>
      <a href="mailto:flaviuscorondan23@gmail.com" class="contact-text">flaviuscorondan23@gmail.com</a>
      <span class="contact-text">(+40) 742070499</span>
    
  </div>


    </header>
    <section class="section">
      <div class="gallery">
        <!-- Proiectul 1 -->
        <div class="project">
          <div class="project-description">
            <h2>Casă Sârbi</h2>
          </div>
          <div class="image-box">
            <span class="expand-indicator">˅</span>
            <div class="image-row">
              <img src="Casa-Archicad.jpg" alt="main-image" class="main-img" />
              <div class="sub-gallery-wrapper">
                <span class="arrow arrow-left" onclick="scrollSubGallery(this, -1)"></span>
                <div class="sub-gallery">
                  <img src="Plan-nivel-1.jpg" alt="Plan" />
                  <img src="Fatada.jpg" alt="Fațada" />
                  <img src="Secțiuni.jpg" alt="Sectiune" />
                  <img src="Toate-Planurile.jpg" alt="Planuri" />
                  <img src="toate-fatadele.jpg" alt="Fatade" />
                  <img src="Toate-sectiunile.jpg" alt="Secțiuni" />
                  <img src="Captura-drona-Casa-editata.jpg" alt="Drona" />
                  <img src="casa-din-metashape.jpg" alt="Cloud" />
                  <img src="casa-elevatie-din-metashape.jpg" alt="DEM" />
                </div>
                <span class="arrow arrow-right" onclick="scrollSubGallery(this, 1)"></span>
              </div>
            </div>
            <div class="prompt" >
             
             În acest proiect am realizat modelarea completă a casei din Sârbi, folosindu-mă de un nor de puncte generat prin fotogrammetrie cu ajutorul unei drone. Pe baza acestuai am creat releveul 2D în AutoCAD, care include planurile, fațadele și secțiunile clădirii. Ulterior, am elaborat un model 3D al clădirii în Archicad.
        
            </div>
          </div>
        </div>
        <!-- Proiectul 2 -->
        <div class="project">
          <div class="project-description">
            <h2>Zona Industrială Calea Buziașului</h2>
          </div>
          <div class="image-box">
            <span class="expand-indicator">˅</span>
            <div class="image-row">
            <img src="CopertaP2.jpg" alt="Plansa-Sit" class="main-img plansa-redusa" />
          <div class="sub-gallery-wrapper">
                <span class="arrow arrow-left" onclick="scrollSubGallery(this, -1)"></span>
                <div class="sub-gallery sub-gallery-large">
              <img src="Plansa-Sit.jpg" alt="Randare 1" />
              <img src="Harta Localizarii.jpg" alt="Randare 2" />
              <img src="distante.jpg" alt="Randare 3" />
              <img src="Limite-si-Bariere.jpg" alt="Randare 4" />
              <img src="Brat-de-deversare si-bazine-de-retentie-a-apei.jpg" alt="Randare 5" />
              <img src="Situatie-actuala.jpg" alt="Randare 6" />
              <img src="toate-diagramele.jpg" alt="Randare 7" />
              <img src="Tipuri-de-drumui.jpg" alt="Randare 8" />
              <img src="Aspecte-Pozitive-si-disfunctionalitati.jpg" alt="Randare 9" />
              <img src="Propunere-Final.jpg" alt="Randare 5" />
              <img src="CUT.jpg" alt="Randare 10" />
              <img src="POT.jpg" alt="Randare 11" />
              <img src="Inaltime.jpg" alt="Randare 12" />
                </div>
                <span class="arrow arrow-right" onclick="scrollSubGallery(this, 1)"></span>
              </div>
            </div>
            <div class="prompt" >
             
             Se urmărește crearea și reamenajarea unui sit urban printr-o abordare rezilientă, care să răspundă atât nevoilor contemporane, cât și să valorifice caracterul existent al locului. Situl a fost împărțit în două mari părți: cea dintâi, Zona 1- situata în partea central- nordică, dinamică, cu caracter urban intens, destinată activităților de tip birouri, locuințe colective, servicii; Cea de-a doua mare zonă,situată în partea sud-estică a zonei centrale, sunt reinterpretări ale elementelor naturale și antropice.
            </div>
          </div>
        </div>  


        <!-- Proiectul 3 -->
        <div class="project">
          <div class="project-description">
            <h2>Autostrada A1 între Deva și Margina</h2>
          </div>
          <div class="image-box">
            <span class="expand-indicator">˅</span>
            <div class="image-row">
            <img src="Coperta.jpg" alt="Plansa-Sit" class="main-img coperta-redusa" />
          <div class="sub-gallery-wrapper">
                <span class="arrow arrow-left" onclick="scrollSubGallery(this, -1)"></span>
                <div class="sub-gallery sub-gallery-large">
              <img src="Harta autostrazilor.jpg" alt="POZA 1" />
              <img src="Localizare.jpg" alt="Imaginea 1" />
              <img src="Amenajari.jpg" alt="Imaginea 1" />
              <img src="Altitudine.jpg" alt="Imaginea 1" />
              <img src="rauri.jpg" alt="Imaginea 1" />
              <img src="Retede-de-transport.jpg" alt="Imaginea 1" />
              <img src="Geologic.jpg" alt="Imaginea 1" />
              <img src="Soluri.jpg" alt="Imaginea 1" />
              <img src="diagrama soluri.jpeg.jpg" alt="Imaginea 1" />
              <img src="Moduri-de-utilizare-a-ternurilor.jpg" alt="Imaginea 1" />
              <img src="Diagrama-utilizarea-terenului.jpg" alt="Imaginea 1" />
              <img src="Firme.jpg" alt="Imaginea 1" />
              <img src="Diagrama firme.jpg" alt="Imaginea 1" />
              <img src="Autostrada-satelit.jpg" alt="Imaginea 1" />
              
             
                </div>
                <span class="arrow arrow-right" onclick="scrollSubGallery(this, 1)"></span>
              </div>
            </div>
            <div class="prompt" >
             
             Sectorul de Autostradă cuprins între Deva și Margina joacă un rol esențial ca patre integrată din structura cuprinzătoare a întregii rețele a Autostrăzi A1. În ansamblu, consecința definitorie a impactului geografic al arealului de studiu este una pozitivă privită din perspectiva subiectelor principale analizate, mai precis în privința componentei mediului, dar și componentei socio-economice.
        
            </div>
          </div>
        </div>  


    
        <!-- Proiectul 4 -->
<div class="project">
  <div class="project-description">
    <h2>Alte Reprezentări</h2>
  </div>

  <!-- 🔽 Aici adăugăm clasa suplimentară -->
  <div class="image-box box-adjust">
    <span class="expand-indicator">˅</span>

    <div class="image-row">
      <div class="sub-gallery-wrapper">
        <span class="arrow arrow-left" onclick="scrollSubGallery(this, -1)"></span>
        <div class="sub-gallery sub-gallery-large">
              <img src="Vila-Plan.jpg" alt="POZA 1" />
             <img src="Fațada-Biserica-Lateral-Stanga.jpg" alt="POZA 1" />
             <img src="fatada-biserca-Principala.jpg" alt="POZA 1" />
             <img src="Fațada-Biserica-Lateral-Dreapta.jpg" alt="POZA 1" />
             <img src="Borne.jpg" alt="POZA 1" />
             <img src="Curbe-de-nivel.jpg" alt="POZA 1" />
             <img src="DTM-si-DEM.jpg" alt="POZA 1" />
             <img src="Suprafață-Teren.jpg" alt="POZA 1" />
             <img src="Suprafețe zone-Varianta1.jpg" alt="POZA 1" />
             <img src="Sectiune-Biserica.jpg" alt="POZA 1" />
             <img src="Sectiune-Vale.jpg" alt="POZA 1" />
             <img src="Propunere Pod.jpg" alt="POZA 1" />
             <img src="Sectiune-Bretea-Sarbi.jpg" alt="POZA 1" />
              
             
                </div>
                <span class="arrow arrow-right" onclick="scrollSubGallery(this, 1)"></span>
              </div>
            </div>
            <div class="prompt" >
             
              Planse aleatorii realizate de-a lungul timpului in diferite programe si moduri. S-au colectat date din teren, a urmat procesarea datelor brute, apoi prelucrarea acestora. Am folosit programul Autocad pentru realizarea planselor de arhitectua, si proiectare a drumurilor. Iar pentru maparea arealelor am folosit softwareul QGIS 
            </div>
          </div>
        </div>  
  
  <div id="lightbox" onclick="closeLightbox()">
    <img id="lightbox-img" src="" alt="Imagine mărită" />
  </div>
  
  <script>
   
    // Funcția openLightbox pentru imaginile din galerie și sub-gallery
    function openLightbox(src, imageType, origWidth) {
      const lightbox = document.getElementById("lightbox");
      const lightboxImg = document.getElementById("lightbox-img");
      lightboxImg.src = src;
      if(imageType === 'profile'){
        lightboxImg.style.setProperty("width", (origWidth * 4) + "px", "important");
      } else {
        lightboxImg.style.width = "95vw";
      }
      lightbox.style.display = "flex";
    }
    
    function closeLightbox() {
      document.getElementById("lightbox").style.display = "none";
    }
    
    // Funcția pentru derularea galeriei în sub-gallery
    function scrollSubGallery(arrow, direction) {
      var wrapper = arrow.parentElement;
      var gallery = wrapper.querySelector(".sub-gallery");
      if (gallery) {
        var scrollAmount = gallery.clientWidth * 0.8;
        gallery.scrollLeft += direction * scrollAmount;
      }
    }
    
    document.addEventListener("DOMContentLoaded", () => {
      const subGalleryImages = document.querySelectorAll(".sub-gallery img");
      subGalleryImages.forEach(img => {
        img.style.cursor = "zoom-in";
        img.addEventListener("click", () => openLightbox(img.src));
      });
      
      const mainImages = document.querySelectorAll(".main-img");
      mainImages.forEach(img => {
        img.style.cursor = "zoom-in";
        img.addEventListener("click", () => openLightbox(img.src));
      });
      
      const profileImages = document.querySelectorAll(".profile-gallery img");
      profileImages.forEach(img => {
        img.style.cursor = "zoom-in";
        img.addEventListener("click", function() {
          openLightbox(this.src, 'profile', this.clientWidth);
        });
      });
    });






    
    document.addEventListener("keydown", (event) => {
      if(event.key === "Escape") {
        closeLightbox();
      }
    });

    document.addEventListener('DOMContentLoaded', () => {
  const projects = document.querySelectorAll('.project');

  projects.forEach(project => {
    // OPEN la hover peste proiect
    project.addEventListener('mouseover', event => {
      if (!project.contains(event.relatedTarget)) {
        // resetează pe toate
        projects.forEach(p => {
          p.classList.remove('project-active');
          p.querySelector('.image-box')?.classList.remove('open');
        });
        // activează pe cel curent
        project.classList.add('project-active');
        project.querySelector('.image-box')?.classList.add('open');
      }
    });

    // CÂND IEȘI DIN .PROJECT → scapi de highlight, închizi și box-ul
    project.addEventListener('mouseleave', () => {
      project.classList.remove('project-active');
      project.querySelector('.image-box')?.classList.remove('open');
    });
  });

  // CÂND IEȘI DIN .IMAGE-BOX (dar încă ești în .project) → doar închizi box-ul
  document.querySelectorAll('.image-box').forEach(box => {
    box.addEventListener('mouseleave', () => {
      box.classList.remove('open');
    });
  });
});





window.addEventListener("load", () => {
  document.querySelectorAll(".prompt").forEach(prompt => {
    const words = prompt.textContent.trim().split(/\s+/);
    let staticText = "", animateWords = words;
    if (words.length > 21) {
      staticText   = words.slice(0, words.length - 21).join(" ");
      animateWords = words.slice(words.length - 21);
    }
    const animatedHTML = animateWords
      .map((w, i) => {
        const delay = (i * 0.125).toFixed(2);  // delay mai mare
        return `<span class="letter" style="animation-delay:${delay}s">${w}</span>`;
      })
      .join(" ");
    prompt.innerHTML = staticText
      ? `${staticText} ${animatedHTML}`
      : animatedHTML;
  });
});





  </script>
</body>
</html>
