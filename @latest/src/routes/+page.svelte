<script>
    import Header1 from '../components/Header1.svelte'; 
    import ProjectCard from '../components/ProjectCard.svelte';
    import Navbar from '../components/Navbar.svelte'; // Import the Navbar component
    import Skills from '../components/Skills.svelte'; 
    

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
<ProjectCard/>
<main class = main-content>


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
  
  </style>
  


