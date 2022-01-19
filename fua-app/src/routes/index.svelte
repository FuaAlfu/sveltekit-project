<script>
    import Title from '$lib/title.svelte';

    //----------------------
    let title = 'my homepage';
    const updateTitle = () => {
        title  = "welcom"
    }
</script>

<Title />
<!-- end of title -->
<div class="index">
    <h2>{title}</h2>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit nam, minus tenetur ab explicabo voluptate quis at tempore cupiditate ex sint quae nihil consectetur. Esse culpa nesciunt accusamus aliquam. Doloremque?</p>

    <button on:click={updateTitle}>Change title</button>
    <input type="text" bind:value={title}><br>
    <a href="/about">About</a>
    <a href="/guides">View Guides</a>
    <a href="/test">Click Me</a>
</div>

<style>
    .index{
        text-align: center;
        display: block;
        margin: 20px auto;
    }
</style>
