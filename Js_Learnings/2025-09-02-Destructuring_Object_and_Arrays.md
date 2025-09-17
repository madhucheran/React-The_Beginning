# Destructuring Objects and Arrays

## Sample Data

```js
const data = [
  {
    id: 1,
    title: "The Lord of the Rings",
    publicationDate: "1954-07-29",
    author: "J. R. R. Tolkien",
    genres: [
      "fantasy",
      "high-fantasy",
      "adventure",
      "fiction",
      "novels",
      "literature",
    ],
    hasMovieAdaptation: true,
    pages: 1216,
    translations: {
      spanish: "El señor de los anillos",
      chinese: "魔戒",
      french: "Le Seigneur des anneaux",
    },
    reviews: {
      goodreads: {
        rating: 4.52,
        ratingsCount: 630994,
        reviewsCount: 13417,
      },
      librarything: {
        rating: 4.53,
        ratingsCount: 47166,
        reviewsCount: 452,
      },
    },
  },
  // ...other books
];
```

```js
function getBooks() {
  return data;
}

function getBook(id) {
  return data.find((d) => d.id === id);
}
```

---

## Destructuring Arrays and Objects

### Traditional Way

```js
const book = getBook(2);

const title = book.title;
const author = book.author;

console.log(author, title);
```

### Using Destructuring

```js
const book = getBook(2);

const {
  title,
  author,
  pages,
  publicationDate,
  genres,
  hasMovieAdaptation,
} = book;

console.log(author, title, pages, publicationDate, genres, hasMovieAdaptation);
```

#### Destructuring Arrays

```js
const [primaryGenre, secondaryGenre] = genres;
console.log(primaryGenre, secondaryGenre);
```

---

> By using destructuring, you can easily extract values from arrays and objects in a concise way.
