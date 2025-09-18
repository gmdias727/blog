+++
title = "Posts"
sort_by = "date"
template = "section.html"
paginate_by = 10
+++

> Here you can read all my articles so far

Last update: <span id="current-date"></span>

Future topics:

Non-Tech Related:

- The struggle I have choosing a path
- Issues with hopping from one programming language to another
- Issues with tech communities in Brazil

Tech Related:

- a

<script>
    const lastUpdate = new Date("September 18, 2025 14:07:00");
    const options = {
        weekday: 'long',
        year: 'numeric',
        month: 'long',
        day: 'numeric'
    };
    const formattedDate = lastUpdate.toLocaleDateString('en-US', options);
    document.getElementById('current-date').textContent = formattedDate;
</script>
