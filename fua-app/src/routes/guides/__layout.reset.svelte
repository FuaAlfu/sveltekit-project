<script>
    import Title from '$lib/title.svelte';
    import '../../styles/global.css';

    // date
//     const date = () => {
//     let currentDate = new Date();
//     let currentYear = currentDate.getFullYear();
//     document.getElementById('d').innerHTML = currentYear.toString();
// }
// date();
</script>

<header>
    <nav>
        <Title title="the awesome tails"/>
        <div class="links">
            <a href="/">HOME</a>
            <a href="/about">About</a>
            <a href="/guides">Guides</a>
        </div>
    </nav>
    <!-- End of nav -->
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
      text-align: center;
      background-color: rgba(0,0,0,1);
  }

  main{
      max-width: 960px;
      margin: 20px auto;
  }

  footer{
      text-align: center;
  }
  .links{
      margin-left: auto;
  }
  a{
      margin-left: 10px;
      text-decoration: none;
  }
  nav{
      display: flex;
      align-items: center;
      max-width: 960px;
      margin: 0 auto;
  }
</style>