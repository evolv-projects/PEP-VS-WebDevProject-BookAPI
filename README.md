# 📚 Book Finder – Frontend JavaScript Project

Build a web application that allows users to search for books using the
**OpenLibrary Search API**, filter and sort results, and view detailed
information about selected books.

---

## 🧠 Background

This project focuses on building a fully functional **client-side web
application** using only HTML, CSS, and JavaScript.

You will use the **OpenLibrary Search API** to fetch book data and dynamically
display search results, allowing users to explore books by **title**, **author**,
or **ISBN**.

This project emphasizes:

- Semantic HTML and responsive CSS  
- Fetching and processing external API data  
- Dynamic DOM manipulation  
- Handling real-world API variability  

---

## ✅ Project Requirements

### 1. 🔍 Search for Books

Implement the `searchBooks(query, type)` function to:

- Accept a **query** and a **type** (`title`, `author`, or `isbn`)
- Fetch results from the **OpenLibrary Search API**
- Return **up to 10** book results
- Gracefully handle empty results

Each returned book object may include:

| Property             | Description                   |
|----------------------|-------------------------------|
| `title`              | Title of the book             |
| `author_name`        | Author(s)                     |
| `isbn`               | ISBN identifier(s)            |
| `cover_i`            | Cover image ID                |
| `ebook_access`       | eBook availability            |
| `first_publish_year` | Year of first publication     |
| `ratings_sortable`   | Numeric or descriptive rating |

> Note: Some fields may be missing depending on the book.

---

### 2. 📄 Display Book Search Results

In `displayBookList()`:

- Render each book as a `<li>` inside `#book-list`
- Each book should display:
  - Title (`.title-element`)
  - Author (`.author-element`)
  - Cover image (`.cover-element`)
  - Rating (`.rating-element`)
  - eBook access info (`.ebook-element`)

---

### 3. 🧾 Handle Search Events

Your HTML must include:

- `<form id="search-form">`
- `<input id="search-input">`
- `<select id="search-type">` (`title`, `author`, `isbn`)
- A submit button

Submitting the form should trigger `handleSearch()`.

---

### 4. 📘 Display Detailed Book Info on Click

When a book is clicked:

- Display detailed info in `#selected-book`
- Show:
  - Title
  - Author(s)
  - Cover image
  - First publish year
  - ISBN
  - eBook access
  - Rating
- Allow returning to the list view

---

### 5. 📊 Sort by Rating

- Include a `<button id="sort-rating">`
- Sort results **descending by rating**
- Missing or non-numeric ratings should be treated as `0`

---

### 6. ✅ Filter by eBook Availability

- Include `<input type="checkbox" id="ebook-filter">`
- When checked, only show books with `ebook_access: "borrowable"`

---

### 7. ♿ Semantic HTML

Use **at least 3 semantic HTML elements**, such as:

- `<header>`
- `<main>`
- `<section>`
- `<article>`
- `<footer>`

---

### 8. 📱 Responsive CSS

Use **at least one** of the following:

- CSS Grid
- Flexbox
- Media Queries

---

## 🌐 OpenLibrary API Reference

### Base Endpoint

```
https://openlibrary.org/search.json
```

### Example Queries

Search by title:
```
https://openlibrary.org/search.json?title=harry%20potter
```

Search by author (via full-text search):
```
https://openlibrary.org/search.json?q=edgar%20allan%20poe
```

Search by ISBN:
```
https://openlibrary.org/search.json?isbn=9781472539342
```

### Cover Images

```
https://covers.openlibrary.org/b/id/{cover_id}-L.jpg
```

---

## 📌 Notes on API Behavior

- Results may vary by query
- Some searches may return empty results
- Metadata is not guaranteed to be complete
- Tests should validate **behavior**, not exact titles

---

## ✅ Final Note

Focus on:

- Robust API handling
- Clean DOM updates
- Defensive coding
- User-friendly behavior

---

**Happy coding! 💻📚**
