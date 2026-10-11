<script setup>
import parrenoImg from '../assets/Profs/parreno-754x1024.jpg.jpeg'
import sapulImg from '../assets/Profs/sapul-754x1024.jpg.jpeg'
import montanoImg from '../assets/Profs/montano-754x1024.jpg.jpeg'
import adorImg from '../assets/Profs/ador-754x1024.jpg.jpeg'
import eregiaImg from '../assets/Profs/eregia-754x1024.jpg.jpeg'
import ojacastroImg from '../assets/Profs/ojacastro-754x1024.jpg.jpeg'
import pajarImg from '../assets/Profs/pajar-754x1024.jpg.jpeg'
import riveraImg from '../assets/Profs/rivera-754x1024.png'
import taasanImg from '../assets/Profs/taasan-754x1024.jpg.jpeg'
import quijanoImg from '../assets/Profs/quijano-e1637132499305.png'

const departments = [
  {
    name: 'MSCS Department',
    people: [
      {
        name: 'Marjee Rose B. Parreno',
        title: 'Department Head',
        image: parrenoImg,
      },
      {
        name: 'Ma. Sheila C. Sapul',
        title: 'Ph.D., Computer Science Faculty',
        image: sapulImg,
      },
      {
        name: 'Antonio M. Montano Jr.',
        title: 'Faculty',
        image: montanoImg,
      },
      {
        name: 'Professor Ador',
        title: 'Faculty Member',
        image: adorImg,
      },
      {
        name: 'Professor Eregia',
        title: 'Faculty Member',
        image: eregiaImg,
      },
    ],
  },
  {
    name: 'BSIT Department',
    people: [
      {
        name: 'Rose Leah Joy A. Ojacastro',
        title: 'Department Head',
        image: ojacastroImg,
      },
      {
        name: 'Lennon D. Pajar',
        title: 'Faculty',
        image: pajarImg,
      },
      {
        name: 'Rhea Mae A. Rivera',
        title: 'Faculty',
        image: riveraImg,
      },
      {
        name: 'Professor Taasan',
        title: 'Faculty Member',
        image: taasanImg,
      },
    ],
  },
]
</script>

<template>
  <section id="faculty" class="faculty-section">
    <div class="section-heading">
      <p class="eyebrow">College of Computer Studies</p>
      <h2>Faculty and Staff</h2>
    </div>

    <section class="dean-feature" aria-label="Dean">
      <h3>Dean</h3>
      <article class="person dean-person">
        <img :src="quijanoImg" alt="Dean Quijano" class="portrait" />
        <h4>Dean Quijano</h4>
      </article>
    </section>

    <section
      v-for="(department, index) in departments"
      :key="department.name"
      class="people-group department-group"
      :aria-labelledby="`department-heading-${index}`"
    >
      <p class="group-kicker">Teaching as a Way of Life</p>
      <h3 :id="`department-heading-${index}`">{{ department.name }}</h3>
      <div class="people-grid">
        <article v-for="person in department.people" :key="person.name" class="person">
          <img :src="person.image" :alt="person.name" class="portrait" />
          <h4>{{ person.name }}</h4>
          <p class="person-title">{{ person.title }}</p>
        </article>
      </div>
    </section>
  </section>
</template>

<style scoped>
.faculty-section {
  padding: 4.5rem 1.5rem 5rem;
  background: #e7e7e7;
  color: #363636;
  scroll-margin-top: 5rem;
}

.section-heading,
.people-group {
  width: min(100%, 900px);
  margin-inline: auto;
  text-align: center;
}

.section-heading {
  margin-bottom: 3.5rem;
}

.dean-feature {
  width: min(100%, 170px);
  margin: 0 auto 4rem;
  text-align: center;
}

.dean-feature h3 {
  margin: 0 0 1rem;
  color: #a1a1a1;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 1.25rem;
  font-weight: 400;
}

.dean-person {
  text-align: center;
}

.dean-person .portrait {
  aspect-ratio: 0.9;
}

.eyebrow,
.group-kicker {
  margin: 0 0 0.4rem;
  color: #737b7d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 0.78rem;
}

.section-heading h2,
.people-group h3 {
  margin: 0;
  color: #a1a1a1;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(1.8rem, 3vw, 2.35rem);
  font-weight: 400;
  line-height: 1.2;
}

.department-group + .department-group {
  margin-top: 4.5rem;
}

.people-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1rem;
  margin: 1.4rem auto 0;
}

.person {
  min-width: 0;
  text-align: left;
}

.portrait {
  display: block;
  width: 100%;
  aspect-ratio: 0.76;
  object-fit: cover;
  object-position: center top;
  border: 1px solid #d9d5c9;
  border-bottom: 3px solid #a1a1a1;
  background: #f1f1f1;
  box-shadow: 0 3px 10px rgba(30, 52, 54, 0.12);
}

.person h4 {
  margin: 0.75rem 0 0.15rem;
  color: #a1a1a1;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 1rem;
  font-weight: 500;
  line-height: 1.3;
}

.person-title,
.department-name {
  margin: 0;
  color: #6f7778;
  font-size: 0.78rem;
  line-height: 1.5;
}

.department-name {
  color: #989e9e;
  font-size: 0.72rem;
}

@media (max-width: 680px) {
  .people-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    max-width: 440px;
    gap: 1.5rem 1rem;
  }

}
</style>
