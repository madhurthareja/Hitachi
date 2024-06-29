<script lang="ts">
  let title: string = "Madhur Thareja";

  const socialLinks = [
    {
      href: "https://madhurthareja.hashnode.dev",
      icon: "fa-brands fa-hashnode",
      text: "Blog",
    },
    {
      href: "https://www.linkedin.com/in/madhurthareja",
      icon: "fa-brands fa-linkedin",
      text: "Linkedin",
    },
    {
      href: "https://github.com/madhurthareja",
      icon: "fa-brands fa-github",
      text: "Github",
    },
    
  ];

  const techStack = [
    [
      { href: "https://www.python.org/", text: "Python" },
      {
        href: "https://developer.mozilla.org/en-US/docs/Web/JavaScript",
        text: "JavaScript",
      },
      { href: "https://www.typescriptlang.org/", text: "TypeScript" },
      { href: "https://cplusplus.com/doc/tutorial/", text: "C++" },
      { href: "https://www.java.com/en/", text: "Java"},
      { href: "https://en.wikipedia.org/wiki/SQL", text: "SQL" },
    ],
    [
      { href: "https://nodejs.org/en/", text: "Node.js" },
      { href: "https://vuejs.org/", text: "Vue" },
      { href: "https://svelte.dev/", text: "Svelte" },
    ],
    [
      { href: "https://numpy.org/", text: "NumPy" },
      { href: "https://pandas.pydata.org/", text: "Pandas" },
      { href: "https://scikit-learn.org/", text: "scikit-learn" },
      { href: "https://pytorch.org/", text: "PyTorch" },
      { href: "https://huggingface.co/", text: "huggingface" },
      { href: "https://www.nltk.org/", text: "NLTK" },
      { href: "https://spacy.io/", text: "spaCy" },
    ],
    [
      { href: "https://www.mysql.com/", text: "MySQL" },
      { href: "https://www.sqlite.org/", text: "SQLite" },
      { href: "https://git-scm.com/", text: "Git" },
      { href: "https://www.kernel.org/", text: "Linux" },
    ],
  ];
</script>

<div id="container--main">
  <section id="wrapper--hero" class="section--page">
      <img
        id="profile-pic"
        src="images/brewphilic.png"
        alt="Gojo Satoru in Shibuya"
        title="Gojo Satoru in Shibuya • Source: @Deltanpopo"
      />

    <div>
      <h1 id="user-name">{title}</h1>
      <p>
        <a
          href="mailto:madhurthareja1105@gmail.com"
          target="_blank"
          rel="noopener noreferrer"
          class="email"
        >
          <i class="fa-solid fa-envelope"></i> madhurthareja1105@gmail.com</a
        >
      </p>
      <p>
        <a class="resume" href="./assets/Resume.pdf" target="_blank"
          ><i class="fa-solid fa-download"></i> Download Resume
        </a>
      </p>
    </div>
  </section>

  <section class="section--page">
    <div id="socials--list">
      {#each socialLinks as { href, icon, text }}
        <a {href} target="_blank" rel="noopener noreferrer" class="profiles">
          <i class={icon}></i>
          {text}
        </a>
      {/each}
    </div>
  </section>

  <section class="section--page">
    <h2><i class="fa-solid fa-bolt"></i> Summary</h2>
    <p>
      I work at the intersection of Electronics & Machine
      Learning focussing on Computer Vision (CV), Generative AI
      (GenAI) and Large Language Models (LLMs). I also have a keen interest in
      cloud, linux and other tools surrounding tech.
      <br />
      <br />
      <small
        >Born and brought up in Gurugram, I lived all of my life there. .</small
      >
    </p>
  </section>
  <section id="work-history-wrapper" class="section--page">
    <h2><i class="fa-solid fa-briefcase"></i> Work</h2>

    <div class="card--work-history">
      👨‍💻 Summer Intern @
      <strong class="company"
        ><a href="https://www.iitrpr.ac.in/" target="_blank" rel="noopener noreferrer"
          >Indian Institute of Technology Ropar</a
        ></strong
      >
      🏢
      <p>
        📅 05/2024 - 07/2024 • Punjab, India 📍
      </p>
    </div>


  <section id="work-history-wrapper" class="section--page">
    <h2><i class="fa-solid fa-graduation-cap"></i> Education</h2>
    <div class="card--work-history">
      <strong>Indian Institute of Technology Madras</strong>
      <p>Bachelor of Science, Electronic Systems</p>
      <p>05/2023 - present</p>
    </div>

    <div class="card--work-history">
      <strong>Birla Institute of Technology and Sciences, Pilani</strong>
      <p>Bachelor of Science, Computer Science</p>
      <p>08/2023 - present</p>
    </div>
  </section>

  <section class="section--page">
    <h2><i class="fa-solid fa-microchip"></i> Tech</h2>

    <div id="wrapper--techstack__items">
      {#each techStack as group}
        <div class="card--techstack">
          <span>
            {#each group as { href, text }, i}
              <a {href} target="_blank" rel="noopener noreferrer">{text}</a
              >{#if i < group.length - 1}
                {", "}
              {/if}
            {/each}
          </span>
        </div>
      {/each}
    </div>
  </section>

  <section class="section--page section--page-text-center footer">
    <a target="_blank" rel="noopener noreferrer" href="https://kit.svelte.dev"
      >Made with <i class="fa-solid fa-heart"></i> using SvelteKit</a
    >
    🚧
    <a
      target="_blank"
      rel="noopener noreferrer"
      href="https://github.com/madhurthareja">Fork me on GitHub</a
    >
  </section>
</div>

<svelte:head>
  <title>{title} • Portfolio</title>
</svelte:head>