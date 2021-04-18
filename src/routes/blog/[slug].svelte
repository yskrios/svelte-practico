<script context="module">
  export async function preload({ params }) {
    const res = await this.fetch(`blog/${params.slug}.json`);
    const data = await res.json();

    if (res.status === 200) {
      return { post: data };
    } else {
      this.error(res.status, data.message);
    }
  }
</script>

<script>
  export let post;
  import readingTime from "../../utils/readingTime";
  import formatIsoTime from "../../utils/formatIsoTime";
</script>

<svelte:head>
  <title>{post.title}</title>
</svelte:head>

<div class="Post">
  <div class="post-title">
    <h2>{post.title}</h2>

    <p class="date">
      <time datetime={post.createdAt}>
        {formatIsoTime(post.createdAt)}
      </time>
      <span>{readingTime(post.html)}</span>
    </p>
  </div>
  <div class="content">
    {@html post.html}
  </div>
  <div class="comments" />
</div>

<style>
  h2 {
    color: #22215b;
    font-size: 28px;
    margin: 0;
    padding: 0;
  }

  .post-title p {
    color: #555;
    font-size: 14px;
    font-weight: 300;
    margin-top: 5px;
    padding: 0;
  }

  .comments {
    margin: 2em 0 0 0;
  }
</style>
