<script>
    export let links = [];
    let showDropdown = false; // Controls dropdown visibility
</script>

<nav>
    <ul class="navbar">
        <li>
            <p>Ben Tranter</p>
        </li>

        <!-- Dropdown for small screens -->
        <div class="dropdown-container">
            <button class="dropdown-btn" on:click={() => {showDropdown = !showDropdown; console.log(showDropdown);}}>
                &#9776; <!-- Hamburger icon -->
            </button>
            {#if showDropdown}
                <ul class="dropdown-content">
                    {#each links as link}
                        <li>
                            <a href={link.href}>{link.text}</a>
                        </li>
                    {/each}
                </ul>
            {/if}
        </div>

        <!-- Links for larger screens -->
        <div class="links">
            {#each links as link}
                <li>
                    <a href={link.href}>{link.text}</a>
                </li>
            {/each}
        </div>
    </ul>
</nav>

<style>
    .navbar {
        display: flex;
        align-items: center;
        list-style: none;
        padding: 0;
        margin: 0;
        background-color: #f7f7f7;
        height: 4rem;
        width: 100%;
        position: relative;
    }

    .links {
        display: flex;
        margin-left: auto;
        margin-right: 2vw;
    }

    .navbar a, .navbar p {
        text-decoration: none;
        color: #080808;
        font-size: 1.2rem;
        padding: 1.4rem 1rem;
    }

    .navbar a:hover {
        background-color: #ffffff;
    }

    .dropdown-container {
        display: none; /* Hidden by default */
    }

    /* Hamburger button */
    .dropdown-btn {
        font-size: 1.8rem;
        background: none;
        border: none;
        cursor: pointer;
        padding: 1rem;
        color: #080808;
    }

    /* Dropdown menu */
    .dropdown-content {
        display: flex;
        flex-direction: column;
        position: absolute;
        top: 4rem;
        right: 2vw;
        background-color: #f7f7f7;
        box-shadow: 0px 10px 16px rgba(0, 0, 0, 0.2);
        z-index: 999;
        padding:0;
        margin:0;
    }

    .dropdown-content li {
        padding: 1rem;
        list-style: none;
    }

    .dropdown-content a {
        color: #080808;
        text-decoration: none;
    }

    .dropdown-content a:hover {
        background-color: #f7f7f7;
        border: dotted black 1px;
    }

    /* Media query for small screens */
    @media (max-width: 768px) {
        .links {
            display: none; /* Hide links on small screens */
        }

        .dropdown-container {
            display: flex;
            margin-left: auto;
            margin-right: 2vw;
        }
    }
</style>
