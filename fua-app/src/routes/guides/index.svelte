<!-- context is special attribute, distinguish between two scripts tag -->
<script context="module">
    export async function load({fetch}){  //export async function load(context)
        //context.fetch();
       const res = await fetch('https://jsonplaceholder.typicode.com/posts');
       const guides = await res.json()

       if(res.ok){
           return{
               props:{
                   guides: guides
               }
           }
       }
       return{
           status: res.status,
           error: new Error("Could not fetch the guides")
       }
    }
</script>

<!-- main script tag -->
<script>
    export let guides
</script>
<div class="guides">
    <ul>
        <!-- <li><a href="/">guide 1</a></li>
        <li><a href="/">guide 1</a></li> -->
        {#each guides as g}
            <li>
                <a herf="/guides">{g.title}</a>
            </li>
        {/each}
    </ul>
</div>

<style>
    .guides{
        margin-top: 20px;
    }
    ul{
        list-style-type: none;
        padding: 0;
    }
    a{
        display: inline-block;
        margin-top: 10px;
        padding: 10px;
        border: 1px dotted rgba(255, 255, 255, 0.2);
    }
</style>