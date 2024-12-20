<script>
    import Header1 from '../components/Header1.svelte'; 
    import Footer from '../components/Footer.svelte';
    import ProjectCard from '../components/ProjectCard.svelte';
    import Navbar from '../components/Navbar.svelte'; // Import the Navbar component
    import Skills from '../components/Skills.svelte'; 
    

    let projects = [
        {
            title: "Michigan College Basketball Database",
            description: "Designed and implemented a database so that local college basketball fans can easily find statistics on their favorite team.",
            link: "https://example.com/project1"
        },
        {
            title: "Zombies Galore",
            description: "Developed a story-based 2D platformer video game using GODOT and GDscript. ",
            link: "https://example.com/project2"
        },
        {
            title: "Portfolio Website",
            description: "The website you're currently viewing, built from scratch using HTML, CSS, JS, and SvelteKit.",
            link: "https://example.com/project3"
        }
    ];

    let skills = [
        "Java",
        "Python",
        "C",
        "HTML/CSS/JS",
        "Machine Learning",
        "Data Structures",
        "Git",
        "Linux"
    ];

    let interests = [
        "oeeoe",
        "Python",
        "C++",
        "HTML/CSS",
        "Machine Learning",
        "Data Structures",
        "Git",
        "Linux"
    ];

    // Define the navigation links
    let navLinks = [
        { text: "Projects", href: "#projects" },
        { text: "Notes", href: "/notes" },
        { text: "Clubs", href: "#clubs" },
        { text: "Blog", href: "#blog" },
        { text: "Papers", href: "#research" },
        { text: "About Me", href: "#aboutme" }
    ];
</script>

<Navbar links={navLinks} /> <!-- Corrected syntax -->
<Header1/>

<main class = main-content>

    <section id="projects">
        <h2>Projects</h2>
        <div class="projects">
            {#each projects as project}
                <ProjectCard {project} />
            {/each}
        </div>
    </section>
    

    <Skills />
    

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact</h2>
        <p>
            Feel free to <a href="mailto:your-email@example.com">email me</a> or connect on 
            <a href="https://www.linkedin.com/in/your-linkedin" target="_blank">LinkedIn</a>.
        </p>
    </section>
</main>

<style>
  p{
    font-family: "Lucida Console", "Courier New", monospace;
  }
  .projects{
    display: flex; /* Use flexbox */
    flex-wrap: wrap; /* Allow cards to wrap */
    justify-content: center; /* Center the cards */
    margin: 0 auto; /* Center the container */
    padding: 20px; /* Add some padding */
  }
  #projects h2{
    margin-top: 2rem;
    text-align: center;
    margin-bottom: 0;
    
    padding-bottom: 0;
    border: 0;
  }
  #projects{
    margin-top: 5rem;
    margin-bottom:0;
  }
  </style>
  

<Footer />
