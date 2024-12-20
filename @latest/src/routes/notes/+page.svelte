<script>
    let subcategories = [
        { name: "Machine Learning", link: "/notes/machine-learning" },
        { name: "Web Development", link: "/notes/web-dev" },
        { name: "Database Design", link: "/notes/database-design" },
        { name: "Parallel Processing", link: "/notes/parallel-processing" }
    ];
</script>

<!-- Grid Layout -->
 <h4>I plan on displaying my knowledge on these topics by providing my notes. The problem is, 90% of my notes are handwritten . I wish I took all my notes on a tablet, it would be much easier to embed them here.</h4>
<div class="grid">
    {#each subcategories as { name, link }}
        <a href={link}>{name}</a>
    {/each}
</div>

<style>
    .grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr); /* 2 columns */
        gap: 20px; /* Spacing between items */
        padding: 20px;
    }

    a {
        text-decoration: none;
        color: #007bff;
        font-size: 1.2rem;
        padding: 10px;
        background-color: #f9f9f9; /* Light background for each link */
        border: 1px solid #ddd;
        text-align: center;
        display: block; /* Makes the link take full grid space */
    }

    a:hover {
        text-decoration: underline;
    }
</style>
