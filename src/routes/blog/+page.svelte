<script>
  import BlogCard from "$lib/components/BlogCard.svelte";

  let posts = [
    {
      title: "How to Select the Perfect Coconut Oil",
      excerpt: "Coconut oil is a versatile and widely used product, but with three main types—virgin, refined, and fractionated—choosing the right one can feel overwhelming.",
      coverImage: "/images/blog/Coconut.jpg",
      authorImage: "/images/authors/leo.jpg",
      author: "Dr. Leo",
      date: "December 13, 2024",
      category: "HERBS",
      href: "/blog/howToSelectThePerfectCoconutOil"
    },
    {
      title: "How to Sanitize Stainless Steel and Glassware",
      excerpt: "The two bottles of hydrosol have been seating on my bookshelf for over 2 years. Hydrosol has very good shelf life...",
      coverImage: "/images/blog/sanitize.jpg",
      authorImage: "/images/authors/leo.jpg",
      author: "Dr. Leo",
      date: "June 4, 2024",
      category: "ANSWERS",
      href: "/blog/howToSanitize"
    },
    {
      title: "Eucalyptus Uses, Benefits and Safety",
      excerpt: "Eucalyptus plant was used traditionally as antiseptic and for respiratory diseases. It helps with colds, flu, sore throats...",
      coverImage: "/images/blog/Eucalyptus.jpg",
      authorImage: "/images/authors/leo.jpg",
      author: "Dr. Leo",
      date: "January 15, 2024",
      category: "EXTRACTION",
      href: "/blog/eucalyptusTree"
    }
  ];
</script>

<section class="max-w-7xl mx-auto px-4 sm:flex sm:flex-col sm:items-center sm:px-6 lg:px-8 py-12">
  <header class="mb-12 text-center">
    <h1 class="text-4xl font-bold text-gray-900">Blog</h1>
    <p class="mt-3 text-gray-600">Latest insights, guides, and tips on herbs and essential oils.</p>
  </header>

  <!-- Blog Grid -->
  <div class="grid gap-8 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3">
    {#each posts as post}
      <BlogCard
        title={post.title}
        excerpt={post.excerpt}
        coverImage={post.coverImage}
        authorImage={post.authorImage}
        author={post.author}
        date={post.date}
        category={post.category}
        href={post.href}
      />
    {/each}
  </div>

  <!-- Pagination (optional) -->
  <div class="mt-12 flex justify-center">
    <nav class="inline-flex space-x-2">
      <a href="#" class="px-4 py-2 border border-gray-300 bg-white text-gray-700 rounded hover:bg-gray-100">Previous</a>
      <a href="#" class="px-4 py-2 border border-gray-300 bg-white text-gray-700 rounded hover:bg-gray-100">Next</a>
    </nav>
  </div>
</section>
