<template>
  <div>
    <!-- <div v-for="(person, index) in people">
      <h1 :key="index">{{ person }}</h1>
    </div>

    <div
      v-for="({ title, author, genre, publicationYear }, index) in books"
      :key="index"
    >
      <h1>{{ author }}</h1>
    </div>

    <ul v-for="(movie, i) in movies" :key="i">
      <li v-for="(el, i) in movie" :key="i">
        {{ el }}
      </li>
    </ul>

    <ul v-for="(value, key, index) in games" :key="index">
      <li>{{ key }} : {{ value }}</li>
    </ul> -->

    <ul v-for="(game, i) in complexGamesObj" :key="i">
      <li>{{ game }}</li>

      <li v-for="(property, i) in game" :key="i">Property: {{ property }}</li>
    </ul>

    <ul v-for="number in 5">
      <li>{{ number }}</li>
    </ul>

    <!-- getting single value from object   -->
  </div>
</template>

<script setup>
import { ref } from "vue";
const people = ref(["Vusal", "Nurlan", "Kanan", "Elvin"]);

const books = ref([
  {
    id: 1,
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    publicationYear: 1960,
  },
  {
    id: 2,
    title: "1984",
    author: "George Orwell",
    genre: "Dystopian",
    publicationYear: 1949,
  },
  {
    id: 3,
    title: "The Great Gatsby",
    author: "F. Scott Fitzgerald",
    genre: "Classic",
    publicationYear: 1925,
  },
  {
    id: 4,
    title: "The Catcher in the Rye",
    author: "J.D. Salinger",
    genre: "Coming-of-age",
    publicationYear: 1951,
  },
  {
    id: 5,
    title: "Harry Potter and the Sorcerer's Stone",
    author: "J.K. Rowling",
    genre: "Fantasy",
    publicationYear: 1997,
  },
]);

const movies = ref([
  [
    "The Shawshank Redemption",
    "The Godfather",
    "The Dark Knight",
    "Schindler's List",
    "The Green Mile",
  ],
  [
    "Pulp Fiction",
    "Fight Club",
    "Forrest Gump",
    "The Silence of the Lambs",
    "The Usual Suspects",
  ],
  [
    "Inception",
    "The Matrix",
    "Interstellar",
    "Blade Runner",
    "Eternal Sunshine of the Spotless Mind",
  ],
  [
    "The Lord of the Rings",
    "Star Wars",
    "Harry Potter",
    "The Hobbit",
    "Jurassic Park",
  ],
  ["Titanic", "Avatar", "The Terminator", "The Sixth Sense", "Gladiator"],
]);

const games = ref({
  id: 1,
  title: "Epic Adventure Game",
  genre: ["Action", "Adventure", "RPG"],
  platform: ["PC", "PlayStation", "Xbox", "Nintendo Switch"],
  releaseDate: "2022-03-15",
  developer: {
    name: "Awesome Game Studios",
    location: "San Francisco, CA",
    teamSize: 50,
  },
  ratings: {
    metacritic: 90,
    user: 4.8,
  },
  features: {
    singlePlayer: true,
    multiplayer: true,
    onlineCoop: true,
    splitScreen: false,
  },
  systemRequirements: {
    minimum: {
      os: "Windows 10",
      processor: "Intel Core i5",
      memory: "8 GB RAM",
      graphics: "NVIDIA GTX 970",
      storage: "50 GB available space",
    },
    recommended: {
      os: "Windows 11",
      processor: "Intel Core i7",
      memory: "16 GB RAM",
      graphics: "NVIDIA RTX 3080",
      storage: "100 GB available space",
    },
  },
  storyline:
    "Embark on a thrilling adventure to save the world from impending doom!",
  characters: ["Hero", "Sidekick", "Villain", "NPCs"],
  achievements: [
    {
      id: 1,
      name: "Master Explorer",
      description: "Explore every corner of the game world",
    },
    {
      id: 2,
      name: "Legendary Warrior",
      description: "Complete the game on the hardest difficulty",
    },
  ],
});

const complexGamesObj = ref({
  game1: {
    title: "Space Explorer",
    genre: "Sci-Fi",
    platform: "PC",
    releaseDate: "2023-05-20",
  },
  game2: {
    title: "Fantasy Quest",
    genre: "Fantasy",
    platform: "PlayStation",
    releaseDate: "2023-07-10",
  },
  movie1: {
    title: "Inception",
    director: "Christopher Nolan",
    genre: "Sci-Fi",
    releaseDate: "2010-07-16",
  },
  movie2: {
    title: "The Shawshank Redemption",
    director: "Frank Darabont",
    genre: "Drama",
    releaseDate: "1994-09-23",
  },
  book1: {
    title: "Dune",
    author: "Frank Herbert",
    genre: "Science Fiction",
    publicationYear: 1965,
  },
  book2: {
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    publicationYear: 1960,
  },
});
</script>

<style scoped></style>
