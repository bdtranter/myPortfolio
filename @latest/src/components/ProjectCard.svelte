<script>
    export let project;
</script>

<article class="project-card">
    <h3>{project.title}</h3>
    <p>{project.description}</p>
    <a href={project.link} target="_blank" rel="noopener">View Project Video (x minutes)</a>
</article>

<style>

    .project-card {
        width:30%; 
        /*max-width: 1000px;*/
        align-items: center;
        border: 2px solid #979595;
        padding: 1rem;
        margin: 1rem .5rem;
        border-radius: 8px;
        transition: transform 0.2s;
        text-indent: 2%;
        background-color: #f7f7f7;
    }
    .project-card a {
    
    margin-left: 2%; /* Indent the link */
    }
    .project-card:hover {
        background-color: white;
    }
    a {
        color: #0070f3;
        text-decoration: none;
    }
    a:hover {
        text-decoration: underline;
    }
    * {
    box-sizing: border-box;
}
</style>
