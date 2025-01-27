<script>
  import { page } from '$app/stores';
  import { onMount } from 'svelte';

  onMount(() => {
    const content = document.querySelector('.docs-content');
    const toc = document.querySelector('#table-of-contents');
    
    if (content && toc) {
      const headings = content.querySelectorAll('h2, h3');
      const tocHtml = Array.from(headings).map(heading => {
        const id = heading.textContent.toLowerCase().replace(/\s+/g, '-');
        heading.id = id;
        const level = heading.tagName === 'H2' ? '' : 'margin-left: 1rem;';
        return `<a href="#${id}" style="${level}">${heading.textContent}</a>`;
      }).join('');
      
      toc.innerHTML = tocHtml;
    }
  });
</script>

<div class="docs-container">
  <article class="docs-content">
    <slot />
  </article>

  <aside class="docs-toc">
    <div class="toc-header">On This Page</div>
    <nav id="table-of-contents">
      <!-- Table of contents will be dynamically populated by JavaScript -->
    </nav>
  </aside>
</div>

<style>
  .docs-container {
    display: flex;
    gap: 2rem;
    height: 100%;
    width: 100%;
  }

  .docs-content {
    width: 900px;
    min-width: 0;
  }

  .docs-toc {
    width: 240px;
    position: sticky;
    top: 2rem;
    height: fit-content;
    padding-left: 1rem;
    border-left: 1px solid var(--border-color);
    flex-shrink: 0;
    margin-left: auto;
  }

  .docs-toc nav {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  .docs-toc a {
    color: #666;
    text-decoration: none;
    font-size: 0.9rem;
    line-height: 1.4;
  }

  .docs-toc a:hover {
    color: #0066cc;
  }

  .toc-header {
    font-weight: 600;
    margin-bottom: 1rem;
    color: #666;
    font-size: 0.875rem;
    text-transform: uppercase;
  }

  @media (max-width: 1024px) {
    .docs-container {
      flex-direction: column;
    }

    .docs-toc {
      display: none;
    }
  }
</style> 