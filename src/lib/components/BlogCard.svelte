<script>
  export let title = "Blog Title";
  export let excerpt = "Short description of the blog post to give a quick overview.";
  export let coverImage = "/images/blog/sample.jpg";
  export let authorImage = "/images/authors/author.jpg";
  export let author = "Dr. Leo";
  export let date = "December 13, 2024";
  export let category = "HERBS";
  export let href = "#";
</script>

<article class="bg-white rounded-lg shadow-md hover:shadow-lg overflow-hidden transition-shadow duration-300">
  <!-- Blog Image with Category -->
  <div class="relative">
    <img src={coverImage} alt={title} class="w-full h-56 object-cover" />
    <span class="absolute top-3 right-3 bg-green-700 text-white text-xs font-semibold px-3 py-1 rounded-full">
      {category}
    </span>
  </div>

  <!-- Card Body -->
  <div class="p-6 text-center">
    <!-- Author avatar (overlap style) -->
    <div class="-mt-12 mb-4 flex justify-center">
      <img src={authorImage} alt={author} class="w-16 h-16 z-10 rounded-full border-4 border-white shadow-md" />
    </div>

    <!-- Title -->
    <h2 class="text-xl font-semibold text-green-700 hover:text-green-900 transition-colors">
      <a href={href}>{title}</a>
    </h2>

    <!-- Excerpt -->
    <p class="mt-3 text-gray-600 text-sm line-clamp-3">{excerpt}</p>

    <!-- Read more -->
    <a href={href} class="mt-4 inline-block text-sm font-semibold text-green-700 hover:underline">
      READ MORE »
    </a>

    <!-- Author + Date -->
    <div class="mt-4 flex justify-center items-center space-x-2 text-sm text-gray-500">
      <span>{author}</span>
      <span>•</span>
      <span>{date}</span>
    </div>
  </div>
</article>
