<template>
  <div class="layout">
    <header class="header">
      <nav class="nav">
        <NuxtLink to="/" class="logo">HS</NuxtLink>
        <div class="nav-links">
          <NuxtLink to="#about" class="nav-link"><span class="nav-number">01.</span> About</NuxtLink>
          <NuxtLink to="#experience" class="nav-link"><span class="nav-number">02.</span> Experience</NuxtLink>
          <NuxtLink to="#skill" class="nav-link"><span class="nav-number">03.</span> Projects</NuxtLink>
          <a href="/resume/resume-Hyungsuk_Do.pdf" class="resume-button" target="_blank" rel="noopener noreferrer">Resume</a>
        </div>
      </nav>
    </header>
    <main class="main">
      <slot />
    </main>
  </div>
</template>

<style>
.layout {
  padding: 0 50px;
}

.header {
  height: 100px;
  display: flex;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: var(--navy);
  z-index: 10;
  padding: 0 50px;
}

.nav {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  color: var(--gold);
  font-size: 24px;
  font-weight: bold;
  /* text-decoration: none; */
}

.nav-links {
  display: flex;
  gap: 30px;
  align-items: center;
}

.nav-link {
  color: var(--lightest-slate);
  text-decoration: none;
  font-size: 13px;
}

.nav-number {
  color: var(--gold);
  margin-right: 5px;
  font-size: 12px;
}

.resume-button {
  color: var(--gold);
  border: 1px solid var(--gold);
  padding: 10px 16px;
  border-radius: 4px;
  text-decoration: none;
  font-size: 13px;
  transition: background-color 0.2s;
}

.resume-button:hover {
  background-color: rgba(100, 255, 218, 0.1);
}

.main {
  padding-top: 100px;
}
</style> 