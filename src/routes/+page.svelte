<script lang="ts">
	// Components
	import DocsLogoAnim from '$libSkeleton/Logo/DocsLogoAnim.svelte';

	// Stores
	import { page } from '$app/stores';
</script>

<div>
	<!-- Hero -->
	<header
		class="variant-glass-surface border-b border-black/5 dark:border-white/5 px-4 py-10 md:py-20"
	>
		<div
			class="container max-w-[1200px] mx-auto grid grid-cols-1 md:grid-cols-2 gap-10 place-items-center md:text-left text-center"
		>
			<!-- Text -->
			<div class="space-y-4 tracking-wide">
				<h1>
					<span class="gradient-heading font-medium text-5xl "
						><small>Hello i am a sausage.</small>
					</span>
				</h1>
				<!-- <h2 class="md:text-4xl">Private and intelligent.</h2> -->
				<div class="text-2xl pb-4 pt-8 md:pt-0 tracking-wide leading-10 font-light">
					These are my favourite sausages:
					<span class="badge variant-soft-primary text-2xl px-4 pb-2">pork</span>
					<span class="badge variant-soft-secondary text-2xl px-4 pb-2">lamb</span> and
					<span class="badge variant-soft-success text-2xl px-4 pb-2">big ones</span><br />
				</div>
				<nav class="md:flex space-x-4 text-center md:text-left">
					{#if $page.data.session}
						<a href="/journal/today" class="btn btn-gradient-primary">
							<span>Go to App</span>
							<span>&rarr;</span>
						</a>
					{:else}
						<a href="/auth/signup" class="btn btn-gradient-primary">
							<span>Sign up</span>
							<span>&rarr;</span>
						</a>
						<a href="/auth/signin" class="btn variant-ghost-surface">Sign in</a>
					{/if}
				</nav>
			</div>
			<!-- Logo -->
			<DocsLogoAnim /> 
		</div>
	</header>

	<div
		class="container max-w-[1200px] mx-auto px-4 py-10 md:py-20 space-y-20 text-center md:text-left"
	>
		<div class="p-4 max-w-2xl mx-auto">
			<span class="text-xl italic">
				AI coach.
			</span>
		</div>

		<!-- Stuff -->
		<section class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
			<h2 class="sr-only">What it can do</h2>
			<div class="card variant-glass-surface p-4 text-center space-y-4">
				<div
					class="bg-primary-800 w-20 mx-auto lg:-mt-10 aspect-square flex justify-center items-center rounded-token shadow"
				>
					<div style="w-10 h-10">
						<span class="fas fa-feather-pointed text-3xl" />
					</div>
				</div>
				<h4>This is a cool feature</h4>
				<p>Bloody good feature explainer text!</p>
			</div>
			<div class="card variant-glass-surface p-4 text-center space-y-4">
				<div
					class="bg-secondary-800 w-20 mx-auto lg:-mt-10 aspect-square flex justify-center items-center rounded-token shadow"
				>
					<span class="fas fa-seedling text-3xl" />
				</div>
				<h4>This is a cool feature</h4>
				<p>Bloody good feature explainer text!</p>
			</div>
			<div class="card variant-glass-surface p-4 text-center space-y-4">
				<div
					class="bg-tertiary-800 w-20 mx-auto lg:-mt-10 aspect-square flex justify-center items-center rounded-token shadow"
				>
					<span class="fas fa-code-branch text-3xl" />
				</div>
				<h4>This is a cool feature</h4>
				<p>Bloody good feature explainer text!</p>
			<div class="card variant-glass-surface p-4 text-center space-y-4">
				<div
					class="bg-success-800 w-20 mx-auto lg:-mt-10 aspect-square flex justify-center items-center rounded-token shadow"
				>
					<span class="fas fa-file-shield text-3xl" />
				</div>
				<h4>This is a cool feature</h4>
				<p>Bloody good feature explainer text!</p>
			</div>
		</section>

		<!-- Pre-Release Alert -->
		<aside class="alert variant-ghost-warning">
			<i class="fa-solid fa-triangle-exclamation text-4xl mx-auto" />
			<div class="alert-message">
				This project is for personal use.
			</div>
			<div class="alert-actions mx-auto">
				<a
					href="https://github.com/wolney8/chatgpt-journal/issues"
					target="_blank"
					rel="noreferrer"
					class="btn variant-filled">Click here for a link</a
				>
			</div>
		</aside>

		<!-- Team -->
		<section class="text-center space-y-6">
			<h2>Created By</h2>
			<ul class="grid grid-cols-1 gap-4 max-w-[800px] mx-auto">
				<li class="card variant-glass-surface p-4 space-y-4">
					<div>
						<h3>Will Olney</h3>
						<p></p>
					</div>
					<div class="flex justify-center space-x-4">
						<a
							class="unstyled"
							href="https://github.com/"
							target="_blank"
							rel="noreferrer"
						>
							<i class="fa-brands fa-github text-xl" />
						</a>
						<a
							class="unstyled"
							href="https://twitter.com/"
							target="_blank"
							rel="noreferrer"
						>
							<i class="fa-brands fa-twitter text-xl" />
						</a>
						<a
							class="unstyled"
							href="https://www.linkedin.com/in/"
							target="_blank"
							rel="noreferrer"
						>
							<i class="fa-brands fa-linkedin text-xl" />
						</a>
					</div>
				</li>
			</ul>
		</section>
	</div>
</div>
