<script>
  import { onMount } from 'svelte'

  const contacts = [
    {
      name: 'John Doe',
      email: 'johndoe@example.com',
      phone: '+1 123-456-7890'
    },
    {
      name: 'Jane Smith',
      email: 'janesmith@example.com',
      phone: '+1 987-654-3210'
    },
    {
      name: 'Mark Johnson',
      email: 'markjohnson@example.com',
      phone: '+1 555-555-5555'
    }
  ]

  onMount(() => {
    // Code to run on component mount
  })
</script>

<style>
  .container {
    max-width: 1200px;
    margin: 20px auto;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }

  table {
    width: 100%;
    border-collapse: collapse;
  }

  th,
  td {
    padding: 10px;
    text-align: left;
    border-bottom: 1px solid #ddd;
  }

  th {
    background-color: #f9f9f9;
    font-weight: bold;
  }

  tr:hover {
    background-color: #f5f5f5;
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
  <table>
    <thead>
      <tr>
        <th>Name</th>
        <th>Email</th>
        <th>Phone</th>
      </tr>
    </thead>
    <tbody>
      {#each contacts as contact}
        <tr>
          <td>{contact.name}</td>
          <td>{contact.email}</td>
          <td>{contact.phone}</td>
        </tr>
      {/each}
    </tbody>
  </table>
</div>

<footer>
  <p>&copy; 2023 My Random Contact Page. All rights reserved.</p>
</footer>
