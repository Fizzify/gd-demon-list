<script>
    export let level;
</script>

<div class="demon-card">
    <h1>{"#" + level.position + " " + level.name}</h1>
    <p>{level.publisher.name}</p>
    <iframe width="560" height="315" src="{level.video.slice(0, 24) + "embed/" + level.video.slice(32, level.video.length)}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<style>
  iframe {
    padding-bottom: 2rem;
  }
</style>
