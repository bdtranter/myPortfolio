
<header>
    
    <div class = "header-content">
        <img class="rounded" src="/benpictest.PNG" alt="">
        <section id="introduction"> 
            <p id="trait1">Driven by curiosity.&nbsp;</p>
            <p id="trait2">Empowered by creativity.</p>
            <p>
                I'm a tech enthusiast who is constantly learning and improving. I love to help others in my industry, and I'm constantly making new connections. I'm a part of GrizzHacks and the Competitive Programming Club at OU. Learn more about me here.
            </p>
        </section>
    
    </div>
</header>

<style>
     .header-content {
        display: flex;
        align-items: center;
        padding: 0 5%; /* Adjusts padding on both sides */
        margin-top: 1rem;
        text-align: left;
    }
    header {
        text-align: center;
        padding: 1.5rem 0;
        background-color: #f7f7f7;
        border-bottom: 2px solid #ddd;
    }
    
    img.rounded {
        border-radius: 50%;
        height: 30vh; 
        margin-right: 5%; /* 10% margin on the right */
    }
    #trait1{
        font-weight: bold;
        margin-right: 0rem;
        
    }
    #trait1, #trait2{
        font-size: 3rem;
        margin-top: 0;
        margin-bottom: 0;
        display: inline;
    }


    @media (max-width: 1050px) {
        img.rounded {
            display: none;
        }
    }
    @media(max-width: 700px){
        #trait1, #trait2{
            font-size: 7vw;
        }
        #trait1::after {
        content: "\A"; /* Adds a line break */
        white-space: pre; /* Ensures the line break is rendered */
        display: inline; /* Inline so it fits naturally in the text */
    }
    }
    @media(max-width: 1450px){
        #trait1::after {
        content: "\A"; /* Adds a line break */
        white-space: pre; /* Ensures the line break is rendered */
        display: inline; /* Inline so it fits naturally in the text */
    }
    }
</style>
