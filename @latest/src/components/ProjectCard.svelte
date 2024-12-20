<script>
    let projects = [
        {
            title: "Michigan College Basketball Database",
            description:
                "Designed and implemented a database so that local college basketball fans can easily find statistics on their favorite team.",
            link: "https://example.com/project1",
        },
        {
            title: "Zombies Galore",
            description:
                "Developed a story-based 2D platformer video game using GODOT and GDscript. ",
            link: "https://example.com/project2",
        },
        {
            title: "Portfolio Website",
            description:
                "The website you're currently viewing, built from scratch using HTML, CSS, JS, and SvelteKit.",
            link: "https://example.com/project3",
        },
    ];
</script>

<section id="projects">
    <h2>My Projects</h2>
    <div class="projects">
        {#each projects as project}
            <article class="project-card">
                <h3>{project.title}</h3>
                <p>{project.description}</p>
                <a href={project.link} target="_blank" rel="noopener"
                    >View Project Video (x minutes)</a
                >
            </article>
        {/each}
    </div>
</section>

<style>
    .project-card {
        width: 30%;
        align-items: center;
        justify-content: space-around;
        border: 2px solid #979595;
        padding: 1rem;
        margin: 1rem 0.5rem;
        border-radius: 8px;
        transition: transform 0.2s;
        text-indent: 2%;
        background-color: #f7f7f7;
    }
    .project-card a {
        margin-left: 2%; /* Indent the link */
        color: #0070f3;
        text-decoration: none;
    }
    .project-card:hover {
        background-color: white;
    }
    a:hover {
        text-decoration: underline;
    }
    * {
        box-sizing: border-box;
    }
    .projects {
        display: flex; /* Use flexbox */
        flex-wrap: wrap; /* Allow cards to wrap */
        justify-content: center; /* Center the cards */
        margin: 0 auto; /* Center the container */
        padding: 20px; /* Add some padding */
    }
    #projects h2 {
        margin-top: 2rem;
        text-align: center;
        margin-bottom: 0;
        padding-bottom: 0;
        border: 0;
        font-size:2.5rem ;
    }
    #projects {
        margin-top: 5rem;
        margin-bottom: 0;
    }
</style>
