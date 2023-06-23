<script>
  import { onMount } from 'svelte'

  const features = [
    {
      title: 'Feature 1',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque semper auctor fermentum.'
    },
    {
      title: 'Feature 2',
      description: 'Nullam in ligula consequat, tempus odio a, gravida felis. Fusce volutpat ipsum vitae leo tempus.'
    },
    {
      title: 'Feature 3',
      description: 'Etiam bibendum dolor vel luctus interdum. Donec iaculis fermentum enim, ac lacinia erat vestibulum et.'
    }
  ]

  onMount(() => {
    // Code to run on component mount
  })
</script>

<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
  }

  header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
  }

  h1 {
    font-size: 36px;
    margin: 0;
  }

  p {
    font-size: 18px;
    margin: 10px 0;
  }

  .container {
    max-width: 1200px;
    margin: 20px auto;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }

  .features {
    display: flex;
    justify-content: center;
    margin-top: 30px;
  }

  .feature {
    width: 300px;
    padding: 20px;
    margin: 0 10px;
    background-color: #f9f9f9;
    text-align: center;
    border-radius: 5px;
  }

  .feature h2 {
    font-size: 24px;
    margin: 0;
    margin-bottom: 10px;
  }

  .feature p {
    color: #777;
  }

  footer {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
    bottom: 0;
    position: absolute;
    width: 97%;
  }

  footer p {
    margin: 0;
  }
</style>

<div class="container">
  <h2>Features</h2>
  <div class="features">
    {#each features as feature}
      <div class="feature">
        <h2>{feature.title}</h2>
        <p>{feature.description}</p>
      </div>
    {/each}
  </div>
</div>

<footer>
  <p>&copy; 2023 My Random Home Page. All rights reserved.</p>
</footer>
