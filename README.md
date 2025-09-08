# 📚 Book Finder – Frontend JavaScript Project

Build a web application that allows users to search for books using the **Google Books API**, filter and sort results, and view detailed information about selected books.

---

## 🧠 Background

In modern web development, the frontend plays a key role in delivering an interactive and engaging user experience. This project focuses on building a fully functional **client-side web application** using only HTML, CSS, and JavaScript.

You will use the **Google Books API** to fetch book data and dynamically display search results, giving users the ability to explore books by title, author, or ISBN.

This project emphasizes:

- Using semantic HTML and responsive CSS
- Fetching and processing external API data with JavaScript
- Dynamically updating the DOM based on user interactions

---

## ✅ Project Requirements

### 1. 🔍 Search for Books

Implement the `searchBooks()` function to:

- Accept a **query** and a **type** (`title`, `isbn`, or `author`).
- Fetch results from the Google Books API.
- Return a **maximum of 10** book results.
- Each book object should include:

  | Property             | Description                   |
  | -------------------- | ----------------------------- |
  | `title`              | Title of the book             |
  | `author_name`        | Author(s)                     |
  | `isbn`               | ISBN identifier               |
  | `cover_i`            | Cover image ID                |
  | `ebook_access`       | Whether it has eBook access   |
  | `first_publish_year` | Year of first publication     |
  | `ratings_sortable`   | Numeric or descriptive rating |

---

### 2. 📄 Display Book Search Results

In `displayBookList()`:

- Render each book as a `<li>` inside an element with id `book-list`.
- Each book should visually show:
  - Title (`.title-element`)
  - Author (`.author-element`)
  - Cover image (`.cover-element`)
  - Rating (`.rating-element`)
  - Ebook access info (`.ebook-element`)

> Layout and order are up to the developer.

---

### 3. 🧾 Handle Search Events

- HTML must include a `<form id="search-form">` with:
  - `<input id="search-input">`
  - `<select id="search-type">` (options: `title`, `isbn`, `author`)
  - `<button id="submit-button">`
- JavaScript should include a `handleSearch()` function triggered on form submission.
  - It should call `searchBooks()` and `displayBookList()`.

---

### 4. 📘 Display Detailed Book Info on Click

When a user clicks a book:

- Show detailed data in an element with `id="selected-book"`.
- Hide the book list (`#book-list`).
- Show the following fields:

  - Title
  - Author
  - Cover image
  - First publish year
  - ISBN
  - Ebook access
  - Rating

Implemented via `displaySingleBook()`.

---

### 5. 📊 Sort by Rating

- Include a `<button id="sort-rating">`.
- On click, call `handleSort()` to sort books **by rating (desc)**.
- Any non-numeric or missing rating should be treated as `"0"`.

---

### 6. ✅ Filter by eBook Availability

- Include a checkbox `<input type="checkbox" id="ebook-filter">`.
- When checked, `handleFilter()` should filter results to show only `borrowable` eBooks.
- When unchecked, all books should be shown.

---

### 7. ♿ Use Semantic HTML Elements

Use **any 3** of the following semantic HTML tags in your HTML:

```html
<article>
  <aside>
    <details>
      <figcaption>
        <figure>
          <footer>
            <header>
              <main>
                <nav><section></section></nav>
              </main>
            </header>
          </footer>
        </figure>
      </figcaption>
    </details>
  </aside>
</article>
```

---

### 8. 📱 Use Responsive CSS

Your `styles.css` should include at least **one** of the following:

- CSS Grid
- Flexbox
- Media Queries

This ensures your app adapts across screen sizes.

---

## 🌐 Google Books API Reference

### Basic Query Format

```
https://www.googleapis.com/books/v1/volumes?q=searchterm
```

> `%20` represents a space.

### Example:

```
https://www.googleapis.com/books/v1/volumes?q=harry%20potter
```

### Searching by Field:

```
https://www.googleapis.com/books/v1/volumes?q=intitle:harry%20potter
https://www.googleapis.com/books/v1/volumes?q=inauthor:Peter%20Loewer
https://www.googleapis.com/books/v1/volumes?q=isbn:1781100500
```

### Limiting Results:

```
https://www.googleapis.com/books/v1/volumes?q=harry%20potter&maxResults=5
```

---

## 📌 Example Response Format (Simplified)

```json
{
  "kind": "books#volumes",
  "totalItems": 1014,
  "items": [
    {
      "kind": "books#volume",
      "volumeInfo": {
        "title": "Harry Potter and the Chamber of Secrets",
        "authors": ["J.K. Rowling"],
        "publishedDate": "2015-12-08",
        "averageRating": 4.5,
        "imageLinks": {
          "thumbnail": "https://..."
        }
      }
    }
  ]
}
```

---

## ✅ Final Note

Focus on:

- Fetching and rendering API data
- Clean, readable DOM manipulation
- Simple and responsive layout
- Clear user experience

---

**Good luck and happy coding! 💻📚**
