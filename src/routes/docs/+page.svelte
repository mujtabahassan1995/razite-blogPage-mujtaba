<script>
    // Example blog data
    const blogs = [
        {
            title: "First Blog Post",
            date: "2024-06-01",
            content: "Welcome to our first blog post! Here we share updates and insights."
        },
        {
            title: "SvelteKit Tips",
            date: "2024-06-05",
            content: "Learn how to use SvelteKit for building fast and modern web apps."
        }
    ];
</script>

<h1>Blog Posts</h1>

{#each blogs as blog}
    <article>
        <h2>{blog.title}</h2>
        <small>{blog.date}</small>
        <p>{blog.content}</p>
    </article>
{/each}