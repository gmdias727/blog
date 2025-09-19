+++
title = "Posts"
sort_by = "date"
template = "section.html"
paginate_by = 10
+++

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
