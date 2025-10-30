<h1>Features</h1>
<p style="color:var(--muted)">Everything you need to run support tickets and streamline your server.</p>

<div style="display:grid; gap:16px; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));">
  {#each Array(6) as _, i}
    <article style="background:var(--surface); border:1px solid var(--border); border-radius: var(--radius); padding:16px;">
      <h3 style="margin:0 0 8px 0;">Card {i+1}</h3>
      <p style="color:var(--muted); margin:0;">Short description about this feature.</p>
    </article>
  {/each}
</div>
