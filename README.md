````markdown
# CineSeek - Movie Discovery Application

## API Overview
The CineSeek application uses the MoviesDatabase API to fetch movie data. 
It allows users to browse movies by year, filter by genre, view movie details, and supports pagination for navigating through results.

## API Version
v1

## Available Endpoints
- `/titles` - Fetches movies with optional filtering by year and genre. Supports pagination.

## Request and Response Format
**Request Example:**
```http
GET /titles?year=2024&genre=Comedy&page=1
````

**Response Example:**

```json
{
  "results": [
    {
      "id": "tt1234567",
      "titleText": { "text": "Example Movie" },
      "releaseYear": { "year": "2024" },
      "primaryImage": { "url": "https://image.url" }
    }
  ]
}
```

## Authentication

All requests require an API key sent in the headers:

```
"x-rapidapi-key": "YOUR_API_KEY"
"x-rapidapi-host": "moviesdatabase.p.rapidapi.com"
```

> **Tip:** Store your API key in a `.env.local` file instead of hardcoding it in your code.

## Error Handling

Common API errors include:

* `404` → Resource not found
* `401` → Unauthorized (invalid API key)
* `500` → Server error

Handle errors using `try/catch` and always check `response.ok` before processing the data.

## Usage Limits and Best Practices

* Use pagination to reduce API request load.
* Cache responses for frequently requested data.
* Store sensitive API keys in environment variables.
* Define TypeScript interfaces for API responses for type safety.
* Implement loading states in the UI while fetching data.

````

---

### ✅ **Instructions**

1. Open your project folder `alx-project-0x14` in VS Code.  
2. Create a new file in the root folder: `README.md`.  
3. Copy and paste the **entire content above** into this file.  
4. Save the file.  
5. Commit and push to GitHub:

```bash
git add README.md
git commit -m "Task 0: Complete README for CineSeek"
git push origin main
