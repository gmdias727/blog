+++
template = "homepage.html"
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
</style>

<div class="homepage-hero">
    <h1 class="homepage-hero-title">Quote of the month</h1>
    <p class="homepage-hero-subtitle">Don't push too much boundaries, you'll be surprised by the fall</p>
    <img src="https://avatars.githubusercontent.com/u/47126700?v=4" alt="pp" width="350" height="350">
    
<div>
    <marquee direction="left"><span id="current-date"></span></marquee>
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

<div >
</div>