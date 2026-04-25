<section>
	<h2>// CSS Variables Linter</h2>
	<p>
		Checks CSS variables: warns unused or undefined vars, errors if used but not
		defined.
	</p>
	<pre><code>npm run lint:css-vars</code></pre>
</section>

<style>
	section {
		margin-bottom: 1.5rem;
	}

	h2 {
		font-size: 1rem;
		color: var(--color-green);
		margin-bottom: 0.5rem;
		font-weight: normal;
	}

	p {
		color: var(--color-text);
		margin-bottom: 0.5rem;
	}

	pre {
		background: var(--color-code-bg);
		padding: 1rem;
		border: 1px solid var(--color-border);
		overflow-x: auto;
	}

	code {
		background: var(--color-code-bg);
		padding: 0.2rem 0.4rem;
		border: 1px solid var(--color-border);
		color: var(--color-blue);
	}
</style>
