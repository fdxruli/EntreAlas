# Taberna Japonesa Inari
***

Taberna Japonesa Inari es una web creada para un restaurante japonés, sus características son:

  * Página web minimalista
  * Full responsive
  * Optimizada para SEO
  * Compatible con la mayoría de navegadores
  * Contiene enlaces a las RRSS más usadas

**Ahora más visual que nunca**
  1. Llena de imágenes atractivas
  2. Totalmente optimizadas
  3. Libres de derechos de autor

## Código en HTML5 y CSS3
Ver [HTML5](https://developer.mozilla.org/es/docs/HTML/HTML5) y [CSS3](https://developer.mozilla.org/es/docs/Archive/CSS3)

## Fuentes personalizadas
`<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;700;800&display=swap" rel="stylesheet">`


## El código HTML implementa galería de imágenes
~~~
<div id="slider-imagenes">
    <div class="slider">
        <img class="img-slider" src="img/slider-atun.jpg" alt="Atún rojo">
        <p class="caption-text">Atún rojo de barbate</p>
    </div>
    <div class="slider">
        <img class="img-slider" src="img/slider-salmon.jpg" alt="Salmón cortado">
        <p class="caption-text">Corte de salmón</p>
    </div>
    <div class="slider">
        <img class="img-slider" src="img/slider-bandeja.jpg" alt="Bandeja de sushi">
        <p class="caption-text">Bandeja de sushi</p>
    </div>
</div>
<div class="botonera-dots">
    <span class="dot" onclick="currentSlide(1)"></span>
    <span class="dot" onclick="currentSlide(2)"></span>
    <span class="dot" onclick="currentSlide(3)"></span>
</div>
~~~
**Con su correspondiente código JS**

~~~
// SLIDWSHOW GALERÍA

var slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("slider");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
}