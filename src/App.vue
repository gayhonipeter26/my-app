<template>

<nav>
  <a href="#about">About</a>
  <a href="#projects">Projects</a>
  <a href="#contact">Contact</a>
</nav>

  <div class="portfolio">

  
  <header>
  <img src="/profile.jpg" alt="Profile picture" class="profile-pic" />
  <h1>Hi, I'm Jane Doe 👩‍💻</h1>
  <p>A beginner web developer learning Vue.js</p>
</header>


    <section>
      <h2>About Me</h2>
      <p>I am learning Vue.js and building my first portfolio site.</p>
    </section>

 <section id="projects">
  <h2>Projects</h2>
  <div class="projects">
    <div class="project-card">
      <h3>🌐 Portfolio Website</h3>
      <p>A simple personal website built with Vue.js</p>
    </div>
    <div class="project-card">
      <h3>📝 To-Do App</h3>
      <p>An app to manage daily tasks efficiently</p>
    </div>
    <div class="project-card">
      <h3>📊 Small Dashboard</h3>
      <p>A dashboard with basic charts and statistics</p>
    </div>
  </div>
</section>


  <section id="contact">
  <h2>Contact</h2>
  <form @submit.prevent="sendMessage">
    <input type="text" v-model="form.name" placeholder="Your Name" required />
    <input type="email" v-model="form.email" placeholder="Your Email" required />
    <textarea v-model="form.message" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
  </form>
</section>

  </div>

  <!-- Footer -->
<footer>
  <p>© 2025 Jane Doe | Built with Vue.js 💚</p>
  <div class="social-links">
    <a href="https://github.com/yourusername" target="_blank">GitHub</a>
    <a href="https://linkedin.com/in/yourusername" target="_blank">LinkedIn</a>
    <a href="https://twitter.com/yourusername" target="_blank">Twitter</a>
  </div>
</footer>

</template>

<script>
export default {
  name: "App",
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: ""
      }
    };
  },
  methods: {
    sendMessage() {
      alert(
        `Thank you, ${this.form.name}! Your message has been sent:\n"${this.form.message}"`
      );
      // reset form
      this.form.name = "";
      this.form.email = "";
      this.form.message = "";
    }
  }
};
</script>



<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

nav {
  background: #2c3e50;
  padding: 10px;
  text-align: center;
}

nav a {
  color: #ecf0f1;
  margin: 0 15px;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  color: #1abc9c;
}

.profile-pic {
  width: 150px;
  height: 150px;
  border-radius: 50%; /* makes it round */
  border: 4px solid white;
  margin-bottom: 20px;
  box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
}


header {
  text-align: center;
  padding: 60px 20px;
  background: linear-gradient(135deg, #1abc9c, #16a085);
  color: white;
  border-radius: 10px;
  margin: 20px 0;
}

header h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

header p {
  font-size: 1.2rem;
  font-style: italic;
}


.portfolio {
  padding: 20px;
  max-width: 800px;
  margin: auto;
}

header {
  text-align: center;
  margin-bottom: 30px;
}

section {
  margin-bottom: 40px;
}

h1, h2 {
  color: #333;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 5px 0;
}

.projects {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.project-card {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0,0,0,0.1);
  transition: transform 0.2s, box-shadow 0.2s;
}

.project-card:hover {
  transform: scale(1.05);
  box-shadow: 0px 6px 15px rgba(0,0,0,0.15);
}

.project-card h3 {
  margin-top: 0;
  color: #2c3e50;
}

.project-card p {
  color: #555;
}

form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
  margin: auto;
}

input, textarea {
  margin: 10px 0;
  padding: 12px;
  border-radius: 6px;
  border: 1px solid #ccc;
  font-size: 1rem;
}

button {
  padding: 12px;
  background: #1abc9c;
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.2s;
}

button:hover {
  background: #16a085;
}

footer {
  text-align: center;
  margin-top: 50px;
  padding: 20px;
  background: #2c3e50;
  color: #ecf0f1;
  border-radius: 10px;
}

.social-links {
  margin-top: 10px;
}

.social-links a {
  margin: 0 10px;
  color: #1abc9c;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.2s;
}

.social-links a:hover {
  color: #16a085;
}

/* =========================
   Mobile Responsive Styles
   ========================= */
@media (max-width: 768px) {
  /* Navbar links stack vertically on smaller screens */
  nav {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  /* Header text smaller */
  header h1 {
    font-size: 1.8rem;
  }

  header p {
    font-size: 1rem;
  }

  /* Profile picture smaller */
  .profile-pic {
    width: 100px;
    height: 100px;
  }

  /* Projects grid: one column instead of multiple */
  .projects {
    grid-template-columns: 1fr;
  }

  /* Form fits nicely on small screens */
  form {
    width: 100%;
    padding: 0 10px;
  }
}


</style>

