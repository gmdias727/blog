+++
template = "homepage.html"

[extra]
comment = true
+++

<style>
.homepage-hero {
    text-align: center;
    padding: 2rem 0;
}

.homepage-hero-title {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.homepage-hero-subtitle {
    font-size: 1.25rem;
    margin-bottom: 1rem;
}

.homepage-navigation {
    margin: 3rem 0;
    padding: 2rem 0;
}

.homepage-navigation h2 {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 2rem;
}

.nav-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
}

.nav-card {
    border: 1px solid var(--border-color, #e9ecef);
    border-radius: 12px;
    padding: 1.5rem;
    text-align: center;
    transition: all 0.3s ease;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.nav-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
    border-color: var(--accent-color, #007bff);
}

.nav-card h3 {
    margin: 0 0 0.5rem 0;
    font-size: 1.25rem;
}

.nav-card p {
    margin: 0 0 1rem 0;
    font-size: 0.9rem;
    line-height: 1.4;
}

.nav-link {
    display: inline-block;
    padding: 0.5rem 1rem;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 500;
    transition: background-color 0.3s ease;
}

.nav-link:hover {
    text-decoration: none;
}

/* Dark theme adjustments */
@media (prefers-color-scheme: dark) {
    .nav-card {
        background: var(--card-bg, #2d3748);
        border-color: var(--border-color, #4a5568);
    }
    
    .nav-card:hover {
        border-color: var(--accent-color, #63b3ed);
    }
}

/* Mobile responsiveness */
@media (max-width: 768px) {
    .nav-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
        padding: 0 0.5rem;
    }
    
    .nav-card {
        padding: 1rem;
    }
    
    .homepage-hero-title {
        font-size: 2rem;
    }
}
</style>

<div class="homepage-hero">
    <h1 class="homepage-hero-title">Quote of the month</h1>
    <p class="homepage-hero-subtitle">Don't push too much boundaries, you'll be surprised by the fall</p>
    <img src="https://avatars.githubusercontent.com/u/47126700?v=4" alt="pp" width="350" height="350">
    
<div>
    <marquee direction="left"><span id="current-date"></span></marquee>
</div>

</div>

<div class="homepage-navigation">

<h2>Explore My Content</h2>

<div class="nav-grid">
    <div class="nav-card">
    <span>📝 Posts</span>
    <p>Technical articles, tutorials, and thoughts</p>
    <a href="/posts" class="nav-link">View All Posts →</a>
</div>

<div class="nav-card">
    <span>🎤 Talks</span>
    <p>Presentations and speaking engagements</p>
    <a href="/talks" class="nav-link">View Talks →</a>
</div>

<div class="nav-card">
    <span>🏷️ Tags</span>
    <p>Browse content by topics and categories</p>
    <a href="/tags" class="nav-link">Explore Tags →</a>
</div>

<div class="nav-card">
    <span>👋 About</span>
    <p>Learn more about me and my background</p>
    <a href="/about" class="nav-link">About Me →</a>
</div>

<div class="nav-card">
    <span>🎯 Hobbies</span>
    <p>What I do when I'm not coding</p>
    <a href="/about/hobbies" class="nav-link">My Hobbies →</a>
</div>

<div class="nav-card">
    <span>📄 Resume</span>
    <p>Professional experience and skills</p>
    <a href="/resume" class="nav-link">View Resume →</a>
</div>
</div>
</div>

<script>
    const today = new Date();
    const options = { 
        weekday: 'long', 
        year: 'numeric', 
        month: 'long', 
        day: 'numeric' 
    };
    const formattedDate = today.toLocaleDateString('en-US', options);
    document.getElementById('current-date').textContent = formattedDate;
</script>

<!-- Comments Section -->
<div class="comments-section">
    <h2>💬 Comments</h2>
    <p>Have thoughts about my blog? Feel free to share them below!</p>
    <div class="giscus"></div>
</div>

<style>
.comments-section {
    margin: 3rem 0;
    padding: 2rem 0;
    border-top: 1px solid var(--border-color, #e9ecef);
}

.comments-section h2 {
    text-align: center;
    margin-bottom: 1rem;
    color: var(--text-color);
}

.comments-section p {
    text-align: center;
    margin-bottom: 2rem;
    color: var(--text-muted, #6c757d);
    font-style: italic;
}

/* Giscus styling */
.giscus {
    margin-top: 2rem;
}

/* Dark theme adjustments for comments */
@media (prefers-color-scheme: dark) {
    .comments-section {
        border-top-color: var(--border-color, #4a5568);
    }
}
</style>
