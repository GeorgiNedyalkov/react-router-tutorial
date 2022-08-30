# React Router Tutorial

- Create a react app
- Install router dependencies

```javascript
npm install react-router-dom@6
```

- Connect the URL
  import BrowserRouter and render it around your whole app
- Add some links
- Add routes folder with two routes Invoices and expenses
- Create Route Config to teach the router how to rende rour app at different URLs

```javascript
import ReactDOM from "react-dom/client"
import { BrowserRouter, Routes, Route } from "react-router-dom"
import App from "./App"
import Expenses from "./routes/expenses"
import Invoices from "./routes/invoices"

const root = ReactDOM.createRoot(document.getElementById("root"))
root.render(
  <BrowserRouter>
    <Routes>
      <Route path="/" element={<App />}>
        <Route path="expenses" element={<Expenses />} />
        <Route path="invoices" element={<Invoices />} />
      </Route>
    </Routes>
  </BrowserRouter>
)
```

- Nested Routes

To avoid repeating shared layouts. We can get automatic, persistent layout handling by doing two things:

1. Nest the routes inside of the App route
2. Render an Outlet

First let's nest the routes. Right now the Expenses and Invoices routes are siblings to the App.
We want to make them children.

We then need to render an "Outlet"

```javascript
import { Outlet, Link } from "react-router-dom"
;<Outlet />
```

- Add Data
- Add No Match Route

```javascript
<Route
  path="*"
  element={
    <main style={{ padding: "1rem" }}>
      <p>There's nothing here!</p>
    </main>
  }
/>
```

- Add a route for each specific invoice
- Create a single invoice component
- Nest that component into the Invoices parent component
- Add an outlet in the parent component
- Display information for the invoices

- Index Routes

- Search Params

- Custom behavior

- Add delete functionality
