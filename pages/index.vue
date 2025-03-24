<template>
  <div class="home">
    <div class="social-links">
      <ul>
        <li>
          <a href="https://github.com/WithNikos" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
          </a>
        </li>
        <li>
          <a href="https://www.linkedin.com/in/hyungsuk-do-1b5799158/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
          </a>
        </li>
        <li>
          <a href="https://twitter.com/" target="_blank" rel="noopener noreferrer" aria-label="Twitter">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path></svg>
          </a>
        </li>
        <li>
          <a href="https://instagram.com/" target="_blank" rel="noopener noreferrer" aria-label="Instagram">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line></svg>
          </a>
        </li>
      </ul>
    </div>

    <section class="hero">
      <p class="greeting">Hi, my name is</p>
      <h1 class="name">Hyungsuk Do</h1>
      <!-- <h2 class="title">I build things for the web.</h2> -->
      <p class="description">
        I was really excited to apply for this job, even though I mostly work on frontend stuff with MPA right now. 
        I think my time with JavaScript and building backend things like REST APIs with ASP.NET gives me a good start to help out in an SPA setup.
        Before our interview, I wanted to learn more about Nuxt and Vue, so I made a little portfolio with Nuxt. 
        It was so much fun—way more lively than MPA—and I loved it. I'd be so happy to bring this excitement to <span class="highlight">Morningstar</span>. 
        I've always looked up to this company in the finance world, and I'd love the chance to learn, grow, and do my best here. 
        <a href="https://github.com/WithNikos" target="_blank" rel="noopener noreferrer" class="company-link">Code for HS's Portfolio</a>.
      </p>
    </section>

    <section id="about" class="about">
      <h2 class="section-heading"><span class="section-number">01.</span> About Me</h2>
      <div class="about-content">
        <div class="about-text">
          <p>
            I am a passionate Full-Stack Developer with a Bachelor of Science in Computer Science from Georgia Institute of Technology. 
            With experience in developing and maintaining scalable web applications, 
            I specialize in C#, ASP.NET Core, SQL Server, JavaScript, and REST API development. 
            My expertise spans both front-end and back-end development, ensuring seamless user experiences and efficient system performance.
          </p>
          <p>
            Currently, I work at the Alabama Department of Public Health, where I work on the development of 
            the Electronic Vital Events Registration System, a web application that manages critical public health records. 
            I am excited about tackling complex challenges, optimizing system efficiency, and building innovative software solutions.
            My passion for software engineering drives me to continuously enhance my skills and contribute to impactful projects.
          </p>
        </div>
        <div class="about-image">
          <img src="/images/myAvatar.png" alt="Hyungsuk Do" />  <!-- // when the image could not be loaded, it will display as the text. -->
        </div>
      </div>
    </section>

    <section id="experience" class="experience">
      <h2 class="section-heading"><span class="section-number">02.</span> Experience</h2>
      <div class="experience-content">
        <div class="tabs">
          <button 
            class="tab-button" 
            :class="{ active: currentTab === 'ADPH' }"
            @click="currentTab = 'ADPH'"
          >Alabama Department of Public Health</button>
          <button 
            class="tab-button" 
            :class="{ active: currentTab === 'HM' }"
            @click="currentTab = 'HM'"
          >Hyundai Mobis North America</button>
        </div>

        <div class="tab-content" v-if="currentTab === 'ADPH'">
          <h3 class="job-title">Full Stack Developer <span class="company">@ Alabama Department of Public Health</span></h3>
          <p class="job-duration">AUG 2022 - Present</p>
          <ul class="job-description">
            <li>Primary developer for the Electronic Vital Events Registration System, managing vital records for hospitals, public health departments, and funeral homes.</li>
            <li>Designed and developed secure, scalable applications using C#, ASP.NET Core, SQL Server, JavaScript, MVC, and REST APIs.</li>
            <li>Developed user-friendly UI components with jQuery, Bootstrap, HTML, and CSS.</li>
            <li>Implemented T-SQL stored procedures for efficient data processing and reporting.</li>
            <li>Integrated third-party APIs to enhance system interoperability and performance.</li>
          </ul>
        </div>

        <div class="tab-content" v-if="currentTab === 'HM'">
          <h3 class="job-title">Full Stack Developer <span class="company">@ Hyundai Mobis North America</span></h3>
          <p class="job-duration">APR 2022 - MAY 2022</p>
          <ul class="job-description">
            <li>Developed enterprise-level web applications supporting vehicle module tracking in manufacturing plants.</li>
            <li>Designed robust backend systems using C#, ASP.NET Core, SQL, and JavaScript.</li>
            <li>Optimized database performance and implemented complex T-SQL queries.</li>
            <li>Conducted system analysis, debugging, and troubleshooting for real-time applications.</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="skill" class="skill">
      <h2 class="section-heading"><span class="section-number">03.</span> Projects</h2>
      
      <div class="featured-projects">
        <!-- ADPH Project -->
        <div class="project">
          <div class="project-image">
            <img src="/images/SampleCertificationForm.png" alt="Sample Image" />
          </div>
          <div class="project-content">
            <p class="project-overline">Current Project</p>
            <h3 class="project-title">Electronic Death Registration System</h3>
            <div class="project-description">
              <p>
                Vital records providers such as funeral homes, physicians, coroners, medical examiners, nursing homes, hospitals, etc., 
                to submit death certificates electronically to the Alabama Department of Public Health, Center for Health Statistics.
              </p>
            </div>
            <ul class="project-tech-list">
              <li>ASP.NET Core</li>
              <li>jQuery-JavaScript</li>
              <li>Bootstrap</li>
              <li>T-SQL</li>
              <li>MSSQL</li>
              <li>REST API</li>
              <li>Telerik UI</li>
              <li>ArcGIS API</li>
              <li>Multiple Pages Application</li>
            </ul>
          </div>
          
        </div>

        <!-- Halcyon Theme Project -->
        <div class="project">
          <div class="project-content">
            <p class="project-overline">Personal Project</p>
            <h3 class="project-title">Pricing of Item - Web Application</h3>
            <div class="project-description">
              <p>
                Pricing service which allows for setting up alerts for prices in online stores and then receive e-mails 
                when prices go under a certain price.
              </p>
            </div>
            <ul class="project-tech-list">
              <li>Python(Flask,Jinja2)</li>
              <li>HTML</li>
              <li>CSS</li>
              <li>Bootstrap</li>
              <li>Mailgun</li>
              <li>MongoDB</li>
            </ul>
            <div class="project-links">
              <a href="https://github.com/nikos1016/price_of_item" target="_blank" rel="noopener noreferrer" aria-label="GitHub Link">
                <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
              </a>
            </div>
          </div>
          <div class="project-image">
            <img src="/images/6.png" alt="Sample Image" />
          </div>
        </div>
      </div>
    </section>

    <!-- side email -->
    <div class="side-email">
      <a href="mailto:grownhs@gmail.com" class="email-link">grownhs@gmail.com</a>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const currentTab = ref('ADPH')
</script>

<style>
.home {
  max-width: 1000px;
  margin: 0 auto;
}

.hero {
  min-height: 80vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 10px;
}

.greeting {
  color: var(--gold);
  font-size: 16px;
  margin-bottom: 5px;
}

.name {
  color: var(--lightest-slate);
  font-size: clamp(40px, 8vw, 80px);
  margin-bottom: 10px;
}

.title {
  color: var(--slate);
  font-size: clamp(40px, 8vw, 80px);
  margin-bottom: 20px;
}

.description {
  max-width: 1080px;
  margin-bottom: 50px;
}

.company-link {
  color: var(--gold);
  text-decoration: none;
}

.cta-button {
  color: var(--gold);
  background-color: transparent;
  border: 1px solid var(--gold);
  border-radius: 4px;
  padding: 20px 28px;
  font-size: 14px;
  text-decoration: none;
  width: fit-content;
  transition: background-color 0.2s;
}

.cta-button:hover {
  background-color: rgba(100, 255, 218, 0.1);
}

.section-heading {
  display: flex;
  align-items: center;
  margin-bottom: 40px;
  font-size: 32px;
  color: var(--lightest-slate);
}

.section-number {
  color: var(--gold);
  font-size: 20px;
  margin-right: 10px;
}

.about {
  padding: 100px 0;
}

.about-content {
  display: grid;
  grid-template-columns: 3fr 2fr;
  gap: 50px;
}

.about-text {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.highlight {
  color: var(--gold);
  text-decoration: none;
}

.about-image img {
  width: 100%;
  max-width: 300px;
  border-radius: 4px;
  filter: grayscale(100%) contrast(1);
  transition: filter 0.2s;
}

.about-image img:hover {
  filter: none;
}

.experience {
  padding: 100px 0;
}

.experience-content {
  display: flex;
  gap: 50px;
}

.tabs {
  display: flex;
  flex-direction: column;
  min-width: 120px;
  border-left: 2px solid var(--lightest-navy);
}

.tab-button {
  all: unset;
  padding: 10px 20px;
  font-size: 13px;
  color: var(--slate);
  cursor: pointer;
  transition: all 0.25s;
  border-left: 2px solid transparent;
  margin-left: -2px;
}

.tab-button:hover {
  color: var(--gold);
  background-color: rgba(100, 255, 218, 0.1);
}

.tab-button.active {
  color: var(--gold);
  border-left-color: var(--gold);
}

.tab-content {
  padding: 10px;
}

.job-title {
  color: var(--lightest-slate);
  font-size: 20px;
  margin-bottom: 5px;
}

.company {
  color: var(--gold);
}

.job-duration {
  font-size: 13px;
  font-family: "SF Mono", monospace;
  margin-bottom: 25px;
}

.job-description {
  list-style: none;
}

.job-description li {
  position: relative;
  padding-left: 30px;
  margin-bottom: 10px;
}

.job-description li::before {
  content: "▹";
  position: absolute;
  left: 0;
  color: var(--gold);
}

.skill {
  padding: 100px 0;
}

.featured-projects {
  display: flex;
  flex-direction: column;
  gap: 50px;
}

.project {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  align-items: center;
}

.project:nth-of-type(2n + 1) .project-content {
  grid-column: 7 / -1;
  text-align: right;
}
.project:nth-of-type(2n) .project-content {
  grid-column: 1 / 7;
}

.project:nth-of-type(2n + 1) .project-tech-list {
  justify-content: flex-end;
}

.project:nth-of-type(2n + 1) .project-links {
  justify-content: flex-end;
}

.project:nth-of-type(2n + 1) .project-image {
  grid-column: 1 / 7;
}
.project:nth-of-type(2n) .project-image {
  grid-column: 7 / -1;  
  text-align: right;
}

.project-content {
  grid-column: 1 / 7;
  position: relative;
  z-index: 2;
}

.project-overline {
  color: var(--green);
  font-family: "SF Mono", monospace;
  font-size: 13px;
  margin-bottom: 10px;
}

.project-title {
  color: var(--gold);
  font-size: clamp(24px, 5vw, 28px);
  margin-bottom: 20px;
}

.project-description {
  background-color: var(--light-navy);
  padding: 25px;
  border-radius: 4px;
  font-size: 14px;
  margin-bottom: 20px;
}

.project-tech-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  list-style: none;
  margin-bottom: 20px;
}

.project-tech-list li {
  color: var(--slate);
  font-family: "SF Mono", monospace;
  font-size: 13px;
  white-space: nowrap;
}

.project-links {
  display: flex;
  gap: 15px;
}

.project-links a {
  color: var(--lightest-slate);
}

.project-links svg {
  width: 20px;
  height: 20px;
}

.project-image {
  grid-column: 6 / -1;
  position: relative;
  z-index: 1;
}

.project-image img {
  width: 80%;
  height: auto;
  border-radius: 4px;
  filter: grayscale(100%) contrast(1);
  transition: filter 0.3s;
}

.project-image:hover img {
  filter: none;
}

@media (max-width: 768px) {
  .project {
    grid-template-columns: 1fr;
  }

  .project-content,
  .project:nth-of-type(2n + 1) .project-content {
    grid-column: 1 / -1;
    text-align: left;
    padding: 20px;
  }

  .project-image,
  .project:nth-of-type(2n + 1) .project-image {
    grid-column: 1 / -1;
  }

  .project-tech-list,
  .project:nth-of-type(2n + 1) .project-tech-list {
    justify-content: flex-start;
  }

  .project-links,
  .project:nth-of-type(2n + 1) .project-links {
    justify-content: flex-start;
  }
}

.contact {
  padding: 100px 0;
  text-align: center;
  max-width: 600px;
  margin: 0 auto;
}

.contact-title {
  color: var(--lightest-slate);
  font-size: clamp(40px, 5vw, 60px);
  margin: 20px 0;
}

.contact-description {
  color: var(--slate);
  margin-bottom: 50px;
}

.contact-button {
  color: var(--gold);
  background-color: transparent;
  border: 1px solid var(--gold);
  border-radius: 4px;
  padding: 20px 28px;
  font-size: 14px;
  text-decoration: none;
  margin-top: 50px;
  transition: all 0.25s;
}

.contact-button:hover {
  background-color: rgba(100, 255, 218, 0.1);
  transform: translateY(-3px);
}

@media (max-width: 768px) {
  .contact {
    padding: 50px 20px;
  }
}

.side-email {
  position: fixed;
  right: 40px;
  bottom: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

.side-email::after {
  content: "";
  display: block;
  width: 1px;
  height: 90px;
  background-color: var(--slate);
}

.email-link {
  color: var(--slate);
  font-family: "SF Mono", monospace;
  font-size: 12px;
  letter-spacing: 0.1em;
  writing-mode: vertical-rl;
  text-decoration: none;
  transition: all 0.25s;
  margin: 20px auto;
}

.email-link:hover {
  color: var(--gold);
  transform: translateY(-3px);
}

@media (max-width: 1080px) {
  .side-email {
    right: 20px;
  }
}

@media (max-width: 768px) {
  .side-email {
    display: none;
  }
}

.social-links {
  position: fixed;
  left: 40px;
  bottom: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.social-links ul {
  display: flex;
  flex-direction: column;
  gap: 20px;
  list-style: none;
  margin: 0;
  padding: 0;
}

.social-links li {
  transition: transform 0.25s;
}

.social-links li:hover {
  transform: translateY(-3px);
}

.social-links a {
  display: inline-block;
  color: var(--slate);
  transition: color 0.25s;
}

.social-links a:hover {
  color: var(--gold);
}

.social-links svg {
  width: 20px;
  height: 20px;
}

.social-links::after {
  content: "";
  display: block;
  width: 1px;
  height: 90px;
  margin-top: 20px;
  background-color: var(--slate);
}

@media (max-width: 1080px) {
  .social-links {
    left: 20px;
  }
}

@media (max-width: 768px) {
  .social-links {
    display: none;
  }
}

</style> 