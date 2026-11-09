<script setup>
import { ref } from 'vue'

const whatsappNumber = '5548988787190'
const whatsappLink = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent('Hola, quiero conocer más sobre Espacio Nórdico.')}`
const menuOpen = ref(false)
const products = [
  {
    name: 'Sillón Nube',
    category: 'Living · Madera natural',
    price: '$ 489.000',
    image:
      'https://images.unsplash.com/photo-1567538096630-e0c55bd6374c?auto=format&fit=crop&w=900&q=85',
    alt: 'Sillón de diseño escandinavo en un ambiente cálido y minimalista',
    tag: 'Más elegido',
  },
  {
    name: 'Mesa Aura',
    category: 'Comedor · Roble macizo',
    price: '$ 625.000',
    image:
      'https://images.unsplash.com/photo-1449247709967-d4461a6a6103?auto=format&fit=crop&w=900&q=85',
    alt: 'Mesa de madera clara en un comedor de estilo nórdico',
    tag: '',
  },
  {
    name: 'Lámpara Bruma',
    category: 'Iluminación · Cerámica',
    price: '$ 128.000',
    image:
      'https://images.unsplash.com/photo-1507473885765-e6ed057f782c?auto=format&fit=crop&w=900&q=85',
    alt: 'Lámpara de mesa cálida sobre una superficie de madera',
    tag: 'Nuevo',
  },
  {
    name: 'Silla Lino',
    category: 'Comedor · Madera y lino',
    price: '$ 215.000',
    image:
      'https://images.unsplash.com/photo-1503602642458-232111445657?auto=format&fit=crop&w=900&q=85',
    alt: 'Silla de diseño minimalista con asiento tapizado',
    tag: '',
  },
  {
    name: 'Mesa de luz Alba',
    category: 'Dormitorio · Madera natural',
    price: '$ 189.000',
    image:
      'https://images.unsplash.com/photo-1499933374294-4584851497cc?auto=format&fit=crop&w=900&q=85',
    alt: 'Mueble auxiliar de madera en un dormitorio sereno',
    tag: '',
  },
  {
    name: 'Sofá Calma',
    category: 'Living · Lino natural',
    price: '$ 890.000',
    image:
      'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=900&q=85',
    alt: 'Sofá claro y confortable en una sala de estar luminosa',
    tag: 'Edición limitada',
  },
]

const benefits = [
  {
    number: '01',
    title: 'Hecho para durar',
    description:
      'Materiales nobles y detalles cuidados. Diseños que vas a querer tener por mucho tiempo.',
    icon: '✳',
  },
  {
    number: '02',
    title: 'Diseño consciente',
    description:
      'Elegimos procesos responsables y proveedores locales para dejar una huella más liviana.',
    icon: '◌',
  },
  {
    number: '03',
    title: 'A tu ritmo',
    description:
      'Te asesoramos de persona a persona para encontrar esa pieza que se siente como tu casa.',
    icon: '↗',
  },
]
</script>

<template>
  <div class="site-shell">
    <div class="announcement">
      <span>DISEÑO QUE SE SIENTE COMO CASA</span>
      <span class="announcement-divider" aria-hidden="true">·</span>
      <span>ENVÍOS A TODO EL PAÍS</span>
    </div>

    <header class="site-header">
      <a class="brand" href="#inicio" aria-label="Espacio Nórdico, inicio">
        <img class="brand-logo" src="/logo-espacio-nordico.png" alt="Espacio Nórdico" />
      </a>

      <button
        class="menu-toggle"
        type="button"
        :aria-expanded="menuOpen"
        aria-controls="main-navigation"
        :aria-label="menuOpen ? 'Cerrar menú' : 'Abrir menú'"
        @click="menuOpen = !menuOpen"
      >
        <span></span>
        <span></span>
      </button>

      <nav id="main-navigation" class="main-navigation" :class="{ 'is-open': menuOpen }">
        <a href="#coleccion" @click="menuOpen = false">Colección</a>
        <a href="#nosotros" @click="menuOpen = false">Nuestra esencia</a>
        <a href="#contacto" @click="menuOpen = false">Contacto</a>
        <a class="nav-cta" :href="whatsappLink" target="_blank" rel="noreferrer">
          Hablemos <span aria-hidden="true">↗</span>
        </a>
      </nav>
    </header>

    <main>
      <section id="inicio" class="hero">
        <div class="hero-copy">
          <p class="eyebrow"><span class="eyebrow-line"></span> OBJETOS PARA HABITAR MEJOR</p>
          <h1>Menos ruido.<br /><em>Más hogar.</em></h1>
          <p class="hero-description">
            Muebles y objetos con alma natural, pensados para acompañar tus días y hacer espacio
            para lo que importa.
          </p>
          <a class="button button-dark" href="#coleccion">
            Descubrí la colección <span aria-hidden="true">↘</span>
          </a>
          <div class="hero-note">
            <span class="note-star" aria-hidden="true">✳</span>
            <span>Diseño simple, hecho para durar.</span>
          </div>
        </div>

        <div class="hero-visual">
          <img
            class="hero-image"
            src="https://images.unsplash.com/photo-1600210492486-724fe5c67fb0?auto=format&fit=crop&w=1600&q=90"
            alt="Living luminoso con muebles naturales y diseño contemporáneo"
            fetchpriority="high"
          />
          <div class="hero-image-caption">
            <span>01 / 03</span>
            <span>La calma también se diseña</span>
          </div>
          <div class="hero-stamp" aria-label="Diseño con intención">
            <span class="stamp-star" aria-hidden="true">✳</span>
            <span>DISEÑO<br />CON INTENCIÓN</span>
          </div>
        </div>
      </section>

      <section id="coleccion" class="collection section-wrap">
        <div class="section-heading">
          <div>
            <p class="eyebrow"><span class="eyebrow-line"></span> PIEZAS CON HISTORIA</p>
            <h2>Elegidas para <em>quedarse.</em></h2>
          </div>
          <p class="section-intro">
            Formas simples, materiales honestos y esa sensación de que todo está en su lugar.
          </p>
        </div>

        <div class="product-grid">
          <article v-for="(product, index) in products" :key="product.name" class="product-card">
            <a
              class="product-image-link"
              :href="`${whatsappLink}%20Estoy%20interesado/a%20en%20${encodeURIComponent(product.name)}.`"
              target="_blank"
              rel="noreferrer"
              :aria-label="`Consultar por ${product.name} en WhatsApp`"
            >
              <div class="product-image-wrap">
                <img
                  :src="product.image"
                  :alt="product.alt"
                  loading="lazy"
                  :style="{ '--image-index': index }"
                />
                <span v-if="product.tag" class="product-tag">{{ product.tag }}</span>
                <span class="product-arrow" aria-hidden="true">↗</span>
              </div>
            </a>
            <div class="product-details">
              <div>
                <h3>{{ product.name }}</h3>
                <p>{{ product.category }}</p>
              </div>
              <span class="product-price">{{ product.price }}</span>
            </div>
          </article>
        </div>

        <div class="collection-note">
          <span>¿Buscás algo especial?</span>
          <a :href="whatsappLink" target="_blank" rel="noreferrer">
            Escribinos, te ayudamos a encontrarlo <span aria-hidden="true">↗</span>
          </a>
        </div>
      </section>

      <section id="nosotros" class="manifesto">
        <div class="manifesto-image">
          <img
            src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&w=1200&q=85"
            alt="Espacio de estar con materiales naturales, plantas y luz de tarde"
            loading="lazy"
          />
          <span class="image-caption">Un hogar que habla de vos.</span>
        </div>
        <div class="manifesto-copy">
          <p class="eyebrow"><span class="eyebrow-line"></span> NUESTRA ESENCIA</p>
          <h2>Lo simple<br />también puede<br /><em>emocionar.</em></h2>
          <p>
            Creemos en los espacios que te hacen bajar un cambio. En la madera que envejece lindo,
            la luz que entra a la tarde y los objetos que cuentan una historia.
          </p>
          <a class="text-link" href="#beneficios">
            Lo que nos mueve <span aria-hidden="true">↘</span>
          </a>
          <div class="manifesto-doodle" aria-hidden="true">✳</div>
        </div>
      </section>

      <section id="beneficios" class="benefits section-wrap">
        <div class="benefits-heading">
          <p class="eyebrow"><span class="eyebrow-line"></span> ELEGIR CON SENTIDO</p>
          <h2>Lo bueno se <em>nota.</em></h2>
        </div>
        <div class="benefit-grid">
          <article v-for="benefit in benefits" :key="benefit.number" class="benefit-card">
            <div class="benefit-topline">
              <span>{{ benefit.number }}</span>
              <span class="benefit-icon" aria-hidden="true">{{ benefit.icon }}</span>
            </div>
            <h3>{{ benefit.title }}</h3>
            <p>{{ benefit.description }}</p>
          </article>
        </div>
      </section>

      <section id="contacto" class="contact-cta">
        <div class="cta-orbit cta-orbit-one" aria-hidden="true"></div>
        <div class="cta-orbit cta-orbit-two" aria-hidden="true"></div>
        <p class="eyebrow"><span class="eyebrow-line"></span> TU PRÓXIMO RINCÓN FAVORITO</p>
        <h2>¿Lo imaginamos<br /><em>juntos?</em></h2>
        <p>Contanos qué tenés en mente. Estamos del otro lado para ayudarte.</p>
        <a class="button button-light" :href="whatsappLink" target="_blank" rel="noreferrer">
          <svg aria-hidden="true" viewBox="0 0 24 24" class="whatsapp-icon">
            <path
              d="M20.52 3.48A11.87 11.87 0 0 0 12.08 0C5.48 0 .11 5.37.11 11.97c0 2.11.55 4.17 1.6 5.99L0 24l6.2-1.63a11.96 11.96 0 0 0 5.87 1.5h.01c6.6 0 11.97-5.37 11.98-11.97a11.9 11.9 0 0 0-3.54-8.42Zm-8.44 18.37h-.01a9.93 9.93 0 0 1-5.06-1.38l-.36-.21-3.68.97.98-3.59-.23-.37a9.92 9.92 0 0 1-1.52-5.3C2.2 6.47 6.64 2.04 12.09 2.04a9.9 9.9 0 0 1 7.04 2.92 9.9 9.9 0 0 1 2.91 7.05c0 5.47-4.45 9.84-9.96 9.84Zm5.46-7.37c-.3-.15-1.77-.87-2.04-.97-.28-.1-.48-.15-.68.15-.2.3-.78.97-.95 1.17-.18.2-.35.23-.65.08-.3-.15-1.27-.47-2.42-1.5-.9-.8-1.5-1.78-1.68-2.08-.18-.3-.02-.46.13-.61.13-.13.3-.35.45-.53.15-.17.2-.3.3-.5.1-.2.05-.38-.03-.53-.07-.15-.67-1.62-.92-2.22-.24-.58-.49-.5-.67-.51h-.57c-.2 0-.53.08-.8.38-.28.3-1.05 1.02-1.05 2.49s1.07 2.89 1.22 3.09c.15.2 2.1 3.2 5.1 4.49.71.3 1.27.49 1.7.62.71.22 1.36.19 1.88.12.57-.09 1.77-.73 2.02-1.44.25-.7.25-1.32.18-1.44-.08-.12-.28-.2-.58-.35Z"
            />
          </svg>
          Hablemos por WhatsApp <span aria-hidden="true">↗</span>
        </a>
        <span class="cta-spark" aria-hidden="true">✳</span>
      </section>
    </main>

    <footer class="site-footer">
      <div class="footer-main">
        <div class="footer-brand-block">
          <a class="brand brand-footer" href="#inicio" aria-label="Espacio Nórdico, inicio">
            <img class="brand-logo" src="/logo-espacio-nordico.png" alt="Espacio Nórdico" />
          </a>
          <p>Diseño que se siente como casa.<br />Hecho para vivirlo todos los días.</p>
        </div>

        <div class="footer-column">
          <h3>Explorá</h3>
          <a href="#coleccion">Colección</a>
          <a href="#nosotros">Nuestra esencia</a>
          <a href="#beneficios">Por qué elegirnos</a>
        </div>

        <div class="footer-column">
          <h3>Hablemos</h3>
          <a :href="whatsappLink" target="_blank" rel="noreferrer">WhatsApp</a>
          <a href="mailto:hola@espacionordico.com">hola@espacionordico.com</a>
          <span>Buenos Aires, Argentina</span>
        </div>

        <a class="back-to-top" href="#inicio" aria-label="Volver al inicio">↑</a>
      </div>
      <div class="footer-bottom">
        <span>© 2026 Espacio Nórdico. Hecho con calma.</span>
        <span>Diseño para vivir más despacio <span aria-hidden="true">✳</span></span>
      </div>
    </footer>

    <a
      class="floating-whatsapp"
      :href="whatsappLink"
      target="_blank"
      rel="noreferrer"
      aria-label="Contactar por WhatsApp"
    >
      <svg aria-hidden="true" viewBox="0 0 24 24">
        <path
          d="M20.52 3.48A11.87 11.87 0 0 0 12.08 0C5.48 0 .11 5.37.11 11.97c0 2.11.55 4.17 1.6 5.99L0 24l6.2-1.63a11.96 11.96 0 0 0 5.87 1.5h.01c6.6 0 11.97-5.37 11.98-11.97a11.9 11.9 0 0 0-3.54-8.42Zm-8.44 18.37h-.01a9.93 9.93 0 0 1-5.06-1.38l-.36-.21-3.68.97.98-3.59-.23-.37a9.92 9.92 0 0 1-1.52-5.3C2.2 6.47 6.64 2.04 12.09 2.04a9.9 9.9 0 0 1 7.04 2.92 9.9 9.9 0 0 1 2.91 7.05c0 5.47-4.45 9.84-9.96 9.84Zm5.46-7.37c-.3-.15-1.77-.87-2.04-.97-.28-.1-.48-.15-.68.15-.2.3-.78.97-.95 1.17-.18.2-.35.23-.65.08-.3-.15-1.27-.47-2.42-1.5-.9-.8-1.5-1.78-1.68-2.08-.18-.3-.02-.46.13-.61.13-.13.3-.35.45-.53.15-.17.2-.3.3-.5.1-.2.05-.38-.03-.53-.07-.15-.67-1.62-.92-2.22-.24-.58-.49-.5-.67-.51h-.57c-.2 0-.53.08-.8.38-.28.3-1.05 1.02-1.05 2.49s1.07 2.89 1.22 3.09c.15.2 2.1 3.2 5.1 4.49.71.3 1.27.49 1.7.62.71.22 1.36.19 1.88.12.57-.09 1.77-.73 2.02-1.44.25-.7.25-1.32.18-1.44-.08-.12-.28-.2-.58-.35Z"
        />
      </svg>
    </a>
  </div>
</template>
