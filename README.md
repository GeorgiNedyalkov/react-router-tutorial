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
      <Route path="/" element={<App />} />
      <Route path="expenses" element={<Expenses />} />
      <Route path="invoices" element={<Invoices />} />
    </Routes>
  </BrowserRouter>
)
```

- Nested Routes

To avoid repeating shared layouts. We can get automatic, persistent layout handling by doing two things:

1. Nest the routes inside of the App route
2. Render an Outlet
