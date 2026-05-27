# Plan: Rebuild index.html (Clean REST Client)

## Background & Motivation
The current workspace contains three different iterations of a REST client (`index.html`, `index2.html`, and `index3.html`). 
- `index.html` is feature-rich but extremely large and complex.
- `index2.html` is too minimal.
- `index3.html` has a great modern UI but lacks some of the advanced features of the first iteration.

The goal is to rebuild a new `index.html` that serves as a "Goldilocks" solution: a single-file, vanilla HTML/JS/CSS REST client that is feature-complete, modern, aesthetically pleasing, and built with clean, maintainable code.

## Scope & Impact
This change will replace the existing `index.html` with a unified, clean version. Furthermore, to ensure a sane and clean workspace, `index2.html` and `index3.html` will be permanently deleted.

## Proposed Solution

The new `index.html` will be structured logically into three main sections:
1.  **CSS Styles:** Modern, responsive design using CSS variables, flexbox/grid, and a polished dark theme (inspired by `index3.html`).
2.  **HTML Structure:** Semantic HTML defining a header, a Request panel, and a Response panel.
3.  **JavaScript Logic:** Clean, modular functions for handling state, UI updates, and network requests.

### Key Features to Implement
*   **Request Configuration:**
    *   Method Selector (GET, POST, PUT, PATCH, DELETE, etc.) with color-coding.
    *   URL Input with auto-formatting.
    *   Tabbed Interface for: Query Parameters, Headers, Request Body (JSON), and Authentication.
    *   Dynamic key-value pair editors for Headers and Params.
*   **Response Handling:**
    *   Meta information display (Status Code, Time in ms, Size in bytes).
    *   Tabbed Interface for: Response Body (with basic JSON syntax highlighting or pretty-printing), Response Headers, and HTML Preview.
*   **Utility & UX:**
    *   Local Storage History: Save recent requests and allow clicking them to repopulate the UI.
    *   "Copy as cURL" functionality.
    *   Loading states during fetch operations.
    *   Clean error handling and display.

## Implementation Steps

1.  **Skeleton Setup:** Create the basic HTML boilerplate with the `<head>` meta tags and basic layout containers (`<header>`, `<main>`, `<section class="panel">`).
2.  **Styling (CSS):** Implement the CSS using CSS variables for theming. Focus on a dark-mode first design with clear input styling, button states, and panel shadows.
3.  **UI Construction (HTML):**
    *   Build the Request panel (Method, URL, Send Button, Tabs, Key-Value lists, Body textarea).
    *   Build the Response panel (Status pill, Meta info, Tabs, Output `<pre>`).
4.  **Core Logic (JavaScript):**
    *   Implement tab switching logic.
    *   Implement the key-value list manager (add row, remove row, collect values).
    *   Implement the `fetch` execution logic, calculating time and size.
    *   Implement Response formatting (JSON parsing and highlighting).
5.  **Advanced Features (JavaScript):**
    *   Implement LocalStorage history saving and rendering.
    *   Implement "Copy cURL" helper.
6.  **Refinement:** Ensure code is thoroughly commented, variables are clearly named, and the overall file remains cohesive.

## Verification
*   Open `index.html` in a modern browser.
*   Test a simple GET request (e.g., `https://jsonplaceholder.typicode.com/posts/1`) and verify the response body, headers, status, time, and size are displayed correctly.
*   Test a POST request with a JSON body and verify it sends correctly.
*   Verify that adding/removing custom headers works.
*   Verify that history items are saved and can be loaded.