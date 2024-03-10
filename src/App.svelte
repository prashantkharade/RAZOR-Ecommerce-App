<script>
  //Pages
  import Login from "./pages/Login.svelte";
  import About from "./pages/About.svelte";
  import Home from "./pages/Home.svelte";
  import Checkout from "./pages/Checkout.svelte";
  import Products from "./pages/Products.svelte";
  import ProductTemplate from "./pages/ProductTemplate.svelte";

  //router
  import { Router, Route, Link } from "svelte-routing";
</script>

<Router>
  <nav class="navbar">
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/products">Products</Link>
    <Link to="/products/5">Products 5</Link>
    <Link to="/products/1">Products 1</Link>
  </nav>
  <Route path="/" component={Home}></Route>
  <Route path="/about" component={About}></Route>
  <Route path="/products" component={Products}></Route>
  <Route path="/products/:id" component={ProductTemplate}></Route>
  <Route path="/login" component={Login}></Route>
</Router>
