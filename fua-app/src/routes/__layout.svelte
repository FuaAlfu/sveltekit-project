<script>
    import Title from '$lib/title.svelte';
    import '../styles/global.css';

    // date
//     const date = () => {
//     let currentDate = new Date();
//     let currentYear = currentDate.getFullYear();
//     document.getElementById('d').innerHTML = currentYear.toString();
// }
// date();
</script>

<header>
  <Title title="the awesome tails"/>
</header>

<main>
<!-- page contetnt -->
  <slot></slot>
</main>

<footer>
   <!-- <p class="date" style="font-size:1.5rem; color:#233233;">&copy; copyright - <span id="d"></span></p> -->
   <p>&copy; copyright 2022 - tails</p>
</footer>

<style>
  header{
      display: flex;
      justify-content: center;
  }

  main{
      max-width: 960px;
      margin: 20px auto;
  }

  footer{
      text-align: center;
  }
</style>