<script>
  import Router from '../Router.svelte'
  import Home from './Home.svelte'
  import Contact from './Contact.svelte'

  const routes = {
    '/': [Home, { message: 'from "/" path' }],
    '/home': [Home, { message: 'from "/home" path' }],
    '/contact': [Contact]
  }
</script>
<div class="header">
  <h1>Welcome to My Website</h1>
  <div style="display: flex;  justify-content: space-between;">
  <a href="#/home" class="btn">Home</a>
  <a href="#/contact" class="btn">Contact</a>
<a href="#/notfound" class="btn">Does not exist</a>
</div>
</div>


<Router routes={routes}>
  <!--
    Content between Router start and end tag will be shown incase of navigation
    to a non-existing route.
   -->
   <div class="container">
    <h1>404 Page Not Found</h1>
    <p>The requested page was not found.</p>
  
  </div>
</Router>

<style>
.header {
    background-color: #333;
    padding: 30px;
    text-align: center;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .header h1 {
    font-size: 36px;
    color: #fff;
    margin: 0;
    letter-spacing: 2px;
  }

  .header .btn {
    background-color: #ff5722;
    color: #fff;
    padding: 13px;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    text-decoration: none;
    transition: background-color 0.3s;
    height: 11px;
    margin-left: 1rem;
  }

  .header .btn:hover {
    background-color: #e64a19;
  }</style>
