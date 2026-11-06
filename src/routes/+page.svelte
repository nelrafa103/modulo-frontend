<script>
	import Button from "#lib/components/button.svelte";
	import Logo from "#lib/assets/614d1097-0a5e-4738-8119-975b124dd369.webp";
	import HeroImage from "#lib/assets/8cba26b5-0bc6-4395-bef8-64d603d91ef4.webp";
	import FeaturesImage from "#lib/assets/image.png";
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>
<main class="md:px-24 px-4 max-w-6xl mx-auto">
	<nav class="py-4 px-2 flex justify-between items-center">
		<div>
			<enhanced:img
				src={Logo}
				class="size-8 rounded-sm"
				width="32"
				height="32"
				alt="Logo"
			/>
		</div>

		<div class="gap-6 flex items-center">
			<div class="space-x-4">
				<a class="text-black font-medium" href="/about">About</a>
				<a class="text-black font-medium" href="#features">Features</a>
				<a class="text-black font-medium" href="#pricing">Pricing</a>
				<a class="text-black font-medium" href="#faqs">FAQs</a>
			</div>
			<Button
				class="justify-self-end"
				as={"a"}
				href={"/register"}
				rel="prefetch">Get started</Button
			>
		</div>
	</nav>
	<section class="mt-12">
		<div class="max-w-3xl">
			<p class="text-sm font-medium text-zinc-500">
				A simpler CMS workflow
			</p>
			<h1
				class="mt-3 text-4xl font-semibold tracking-tight text-zinc-950 sm:text-5xl"
			>
				A better way to manage your content
			</h1>
			<p class="mt-1 mb-4 max-w-2xl text-lg leading-7 text-zinc-600">
				Create, organize, and publish everything in one simple
				workspace.
			</p>

			<Button data-variant="outline" as={"a"} href="/login" rel="prefetch"
				>Sign in</Button
			>
		</div>
		<enhanced:img
			src={HeroImage}
			class="mt-10 w-full rounded-md"
			alt="CMS mascot against a blue background"
		/>
	</section>

	<section
		aria-label="Platform statistics"
		class="mt-12 grid grid-cols-2 gap-6 border-y border-zinc-200 py-10 md:grid-cols-4 md:gap-8"
	>
		{#each [{ value: "100", label: "Projects" }, { value: "2000", label: "Customers" }, { value: "1,000,000", label: "Requests per minute" }, { value: ">200ms", label: "Response time for 99% of users" }] as stat}
			<article
				class="border-l border-zinc-200 pl-4 first:border-0 first:pl-0"
			>
				<p class="text-3xl font-semibold tracking-tight text-zinc-950">
					{stat.value}
				</p>
				<h2 class="mt-2 text-sm leading-5 text-zinc-600">
					{stat.label}
				</h2>
			</article>
		{/each}
	</section>

	<section id="features" class="mt-12 scroll-mt-8 border-zinc-200 py-16">
		<div class="grid gap-8 md:grid-cols-[1fr_2fr] md:gap-12">
			<div>
				<p class="text-gray-400 text-sm font-medium">Features</p>
				<h2
					class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
				>
					Everything your content needs
				</h2>
				<p class="mt-4 leading-7 text-zinc-600">
					Create, organize, and publish content with tools that keep
					your workflow simple.
				</p>
			</div>

			<ul class="grid gap-x-8 md:grid-cols-2">
				<li class="flex gap-4 border-t border-zinc-200 py-6">
					<div
						class="feature-sprite aspect-square shrink-0"
						style="--sprite-x: 0%; --sprite-y: 50%;"
						aria-hidden="true"
					></div>
					<div>
						<h2 class="font-semibold text-zinc-950">
							Flexible content editing
						</h2>
						<p class="mt-2 text-sm leading-6 text-zinc-600">
							Write and format content in a clear, easy-to-use
							editor.
						</p>
					</div>
				</li>
				<li class="flex gap-4 border-t border-zinc-200 py-6">
					<div
						class="feature-sprite aspect-square shrink-0"
						style="--sprite-x: 100%; --sprite-y: 0%;"
						aria-hidden="true"
					></div>
					<div>
						<h2 class="font-semibold text-zinc-950">
							Media in one place
						</h2>
						<p class="mt-2 text-sm leading-6 text-zinc-600">
							Keep the images and assets for your projects
							organized.
						</p>
					</div>
				</li>
				<li class="flex gap-4 border-t border-zinc-200 py-6">
					<div
						class="feature-sprite aspect-square shrink-0"
						style="--sprite-x: 66.67%; --sprite-y: 50%;"
						aria-hidden="true"
					></div>
					<div>
						<h2 class="font-semibold text-zinc-950">
							Find content faster
						</h2>
						<p class="mt-2 text-sm leading-6 text-zinc-600">
							Quickly locate the content and assets you need.
						</p>
					</div>
				</li>
				<li class="flex gap-4 border-t border-zinc-200 py-6">
					<div
						class="feature-sprite aspect-square shrink-0"
						style="--sprite-x: 100%; --sprite-y: 50%;"
						aria-hidden="true"
					></div>
					<div>
						<h2 class="font-semibold text-zinc-950">
							Secure by design
						</h2>
						<p class="mt-2 text-sm leading-6 text-zinc-600">
							Help keep your content and workspace protected.
						</p>
					</div>
				</li>
				<li class="flex gap-4 border-t border-zinc-200 py-6">
					<div
						class="feature-sprite aspect-square shrink-0"
						style="--sprite-x: 0%; --sprite-y: 100%;"
						aria-hidden="true"
					></div>
					<div>
						<h2 class="font-semibold text-zinc-950">
							Track performance
						</h2>
						<p class="mt-2 text-sm leading-6 text-zinc-600">
							Get a clearer view of how your content is doing.
						</p>
					</div>
				</li>
				<li class="flex gap-4 border-t border-zinc-200 py-6">
					<div
						class="feature-sprite aspect-square shrink-0"
						style="--sprite-x: 100%; --sprite-y: 100%;"
						aria-hidden="true"
					></div>
					<div>
						<h2 class="font-semibold text-zinc-950">
							Publish with confidence
						</h2>
						<p class="mt-2 text-sm leading-6 text-zinc-600">
							Keep your publishing workflow clear from draft to
							done.
						</p>
					</div>
				</li>
			</ul>

			<div></div>
			<div class="mt-3 flex justify-end">
				<a
					href="/features#content-editor"
					class="text-sm font-medium text-zinc-950 underline underline-offset-4"
				>
					See more
				</a>
			</div>
		</div>
	</section>

	<section id="pricing" class="mt-20 scroll-mt-8 pb-16">
		<div class="max-w-2xl">
			<p class="text-gray-400 text-sm font-medium">Pricing</p>
			<h2
				class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
			>
				Simple plans that grow with you
			</h2>
			<p class="mt-3 text-zinc-600">
				Start with the essentials and upgrade when your team is ready.
			</p>
		</div>

		<div
			class="mt-10 grid grid-cols-1 divide-y divide-zinc-200 md:grid-cols-3 md:divide-x md:divide-y-0"
		>
			<article class="py-8 md:py-0 md:pr-8">
				<h3 class="font-semibold text-zinc-950">Starter</h3>
				<p
					class="mt-4 text-4xl font-semibold tracking-tight text-zinc-950"
				>
					$0
					<span class="text-base font-normal text-zinc-500"
						>/ month</span
					>
				</p>
				<p class="mt-3 min-h-12 text-sm text-zinc-600">
					Everything you need to get started.
				</p>
				<ul class="mt-6 space-y-3 text-sm text-zinc-700">
					<li>1 project</li>
					<li>Core features</li>
					<li>Community support</li>
				</ul>
				<a
					href="/"
					class="mt-8 inline-flex font-medium text-zinc-950 underline underline-offset-4"
				>
					Get started
				</a>
			</article>

			<article class="py-8 md:px-8 md:py-0">
				<h3 class="font-semibold text-zinc-950">Pro</h3>
				<p
					class="mt-4 text-4xl font-semibold tracking-tight text-zinc-950"
				>
					$19
					<span class="text-base font-normal text-zinc-500"
						>/ month</span
					>
				</p>
				<p class="mt-3 min-h-12 text-sm text-zinc-600">
					More room to build and collaborate.
				</p>
				<ul class="mt-6 space-y-3 text-sm text-zinc-700">
					<li>Unlimited projects</li>
					<li>Advanced features</li>
					<li>Priority support</li>
				</ul>
				<a
					href="/"
					class="mt-8 inline-flex font-medium text-zinc-950 underline underline-offset-4"
				>
					Choose Pro
				</a>
			</article>

			<article class="py-8 md:pl-8 md:py-0">
				<h3 class="font-semibold text-zinc-950">Team</h3>
				<p
					class="mt-4 text-4xl font-semibold tracking-tight text-zinc-950"
				>
					$49
					<span class="text-base font-normal text-zinc-500"
						>/ month</span
					>
				</p>
				<p class="mt-3 min-h-12 text-sm text-zinc-600">
					Tools and support for growing teams.
				</p>
				<ul class="mt-6 space-y-3 text-sm text-zinc-700">
					<li>Everything in Pro</li>
					<li>Team access</li>
					<li>Dedicated support</li>
				</ul>
				<a
					href="/"
					class="mt-8 inline-flex font-medium text-zinc-950 underline underline-offset-4"
				>
					Choose Team
				</a>
			</article>
		</div>
	</section>

	<section id="faqs" class="mt-20 scroll-mt-8 pb-16">
		<div class="max-w-2xl">
			<p class="text-gray-400 text-sm font-medium">FAQs</p>
			<h2
				class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
			>
				Frequently asked questions
			</h2>
		</div>

		<div
			class="mt-8 max-w-3xl divide-y divide-zinc-200 border-y border-zinc-200"
		>
			<details>
				<summary class="cursor-pointer py-5 font-medium text-zinc-950">
					Which plan is right for me?
				</summary>
				<p class="pb-5 text-sm leading-6 text-zinc-600">
					Starter is a good place to begin, Pro adds room for more
					projects and collaboration, and Team is designed for growing
					teams.
				</p>
			</details>
			<details>
				<summary class="cursor-pointer py-5 font-medium text-zinc-950">
					What’s included in the Starter plan?
				</summary>
				<p class="pb-5 text-sm leading-6 text-zinc-600">
					Starter includes one project, core features, and community
					support at no monthly cost.
				</p>
			</details>
			<details>
				<summary class="cursor-pointer py-5 font-medium text-zinc-950">
					Are the prices billed monthly?
				</summary>
				<p class="pb-5 text-sm leading-6 text-zinc-600">
					Yes. The Pro and Team prices shown are per month.
				</p>
			</details>
			<details>
				<summary class="cursor-pointer py-5 font-medium text-zinc-950">
					What support is available?
				</summary>
				<p class="pb-5 text-sm leading-6 text-zinc-600">
					Starter includes community support, Pro includes priority
					support, and Team includes dedicated support.
				</p>
			</details>
		</div>
	</section>

	<section
		class="mt-20 grid items-center gap-10 border-t border-zinc-200 py-16 md:grid-cols-2"
	>
		<img
			src={FeaturesImage}
			class="w-full rounded-md"
			alt="Illustration of the Vite+ unified toolchain"
		/>
		<div>
			<p class="text-gray-400 text-sm font-medium">
				More than a build tool
			</p>
			<h2
				class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
			>
				Your whole workflow, working together
			</h2>
			<p class="mt-4 leading-7 text-zinc-600">
				Bring development, builds, and everyday tasks into one
				streamlined toolchain, so you can spend less time switching
				tools and more time building.
			</p>
			<ul class="mt-6 space-y-3 text-sm text-zinc-700">
				<li>One unified frontend workflow</li>
				<li>Fast development and production builds</li>
				<li>Tools designed to work together</li>
			</ul>
		</div>
	</section>

	<section id="testimonials" class="border-t border-zinc-200 py-16">
		<div class="max-w-2xl">
			<p class="text-gray-400 text-sm font-medium">Testimonials</p>
			<h2
				class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
			>
				What teams say
			</h2>
			<p class="mt-3 text-sm text-zinc-600">
				Sample quotes below—replace these with feedback from your
				customers.
			</p>
		</div>

		<div
			class="mt-10 grid grid-cols-1 divide-y divide-zinc-200 md:grid-cols-3 md:divide-x md:divide-y-0"
		>
			<figure class="py-6 md:py-0 md:pr-8">
				<blockquote class="text-lg leading-7 text-zinc-800">
					“Everything feels easier to manage when the tools work
					together.”
				</blockquote>
				<figcaption class="mt-5 text-sm">
					<span class="block font-medium text-zinc-950"
						>Customer name</span
					>
					<span class="mt-1 block text-zinc-500">Role, Company</span>
				</figcaption>
			</figure>

			<figure class="py-6 md:px-8 md:py-0">
				<blockquote class="text-lg leading-7 text-zinc-800">
					“We spend less time switching between tools and more time
					building.”
				</blockquote>
				<figcaption class="mt-5 text-sm">
					<span class="block font-medium text-zinc-950"
						>Customer name</span
					>
					<span class="mt-1 block text-zinc-500">Role, Company</span>
				</figcaption>
			</figure>

			<figure class="py-6 md:pl-8 md:py-0">
				<blockquote class="text-lg leading-7 text-zinc-800">
					“The workflow is simple to pick up and fits naturally into
					our work.”
				</blockquote>
				<figcaption class="mt-5 text-sm">
					<span class="block font-medium text-zinc-950"
						>Customer name</span
					>
					<span class="mt-1 block text-zinc-500">Role, Company</span>
				</figcaption>
			</figure>
		</div>
	</section>

	<section id="api-sdk" class="border-t border-zinc-200 py-16">
		<div class="grid gap-8 md:grid-cols-[1fr_2fr] md:gap-12">
			<div>
				<p class="text-gray-400 text-sm font-medium">For developers</p>
				<h2
					class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
				>
					Build on top of your content
				</h2>
				<p class="mt-4 leading-7 text-zinc-600">
					Connect your projects to the tools and workflows you already
					use with the API and SDK.
				</p>
				<ul
					aria-label="Programming languages"
					class="mt-6 flex flex-wrap gap-2"
				>
					{#each ["Python", "JavaScript", "TypeScript", "Go", "Ruby", "PHP", "Java", "C#", "Rust", "Kotlin", "Swift", "Elixir"] as language}
						<li>
							<span
								class="inline-flex rounded-full border border-zinc-200 bg-white px-3 py-1.5 text-sm font-medium text-zinc-700"
							>
								{language}
							</span>
						</li>
					{/each}
				</ul>
			</div>

			<div class="grid gap-6 md:grid-cols-2">
				<article class="border-t border-zinc-200 py-6">
					<p class="text-xs font-medium text-zinc-500">
						REST API · Python
					</p>
					<h3 class="mt-2 text-lg font-semibold text-zinc-950">
						API
					</h3>
					<p class="mt-3 text-sm leading-6 text-zinc-600">
						Work with your project content programmatically and
						build custom integrations around your workflow.
					</p>
					<pre
						aria-label="Python example using the REST API"
						class="mt-5 overflow-x-auto rounded-md border border-zinc-200 bg-white p-4 text-xs leading-6 text-zinc-800"><code
							><span class="font-semibold text-violet-700"
								>import</span
							> <span class="text-sky-700">requests</span>

response = <span class="text-sky-700">requests</span>.<span
								class="font-semibold text-blue-700">get</span
							>(
    <span class="text-emerald-700">"https://api.example.com/v1/projects"</span>,
    headers=&#123;<span class="text-emerald-700">"Authorization"</span>: <span
								class="text-emerald-700"
								>"Bearer YOUR_API_KEY"</span
							>&#125;,
)
response.<span class="font-semibold text-blue-700">raise_for_status</span>()
projects = response.<span class="font-semibold text-blue-700">json</span
							>()</code
						></pre>
				</article>
				<article class="border-t border-zinc-200 py-6">
					<p class="text-xs font-medium text-zinc-500">
						Python SDK · Example
					</p>
					<h3 class="mt-2 text-lg font-semibold text-zinc-950">
						SDK
					</h3>
					<p class="mt-3 text-sm leading-6 text-zinc-600">
						Use a developer-friendly client to integrate the API
						from your application with less repetitive code.
					</p>
					<pre
						aria-label="Python example using the SDK"
						class="mt-5 overflow-x-auto rounded-md border border-zinc-200 bg-white p-4 text-xs leading-6 text-zinc-800"><code
							><span class="font-semibold text-violet-700"
								>from</span
							> <span class="text-sky-700">your_sdk</span> <span
								class="font-semibold text-violet-700"
								>import</span
							> <span class="text-sky-700">Client</span>

client = <span class="text-sky-700">Client</span>(api_key=<span
								class="text-emerald-700">"YOUR_API_KEY"</span
							>)
projects = client.projects.<span class="font-semibold text-blue-700">list</span
							>()</code
						></pre>
				</article>
			</div>
		</div>
	</section>

	<section
		id="team"
		aria-labelledby="team-heading"
		class="border-t border-zinc-200 py-16"
	>
		<div class="max-w-2xl">
			<p class="text-gray-400 text-sm font-medium">Our team</p>
			<h2
				id="team-heading"
				class="mt-3 text-3xl font-semibold tracking-tight text-zinc-950"
			>
				The people behind the product
			</h2>
			<p class="mt-3 leading-7 text-zinc-600">
				A focused team bringing product, engineering, and quality
				together.
			</p>
		</div>

		<div class="mt-10 grid gap-x-8 gap-y-6 sm:grid-cols-2 md:grid-cols-3">
			<article class="border-t border-zinc-200 py-5">
				<h3 class="font-semibold text-zinc-950">Developer</h3>
				<p class="mt-2 text-sm leading-6 text-zinc-600">
					Builds and maintains product features.
				</p>
			</article>
			<article class="border-t border-zinc-200 py-5">
				<h3 class="font-semibold text-zinc-950">Developer</h3>
				<p class="mt-2 text-sm leading-6 text-zinc-600">
					Improves the tools and workflows customers use.
				</p>
			</article>
			<article class="border-t border-zinc-200 py-5">
				<h3 class="font-semibold text-zinc-950">CEO</h3>
				<p class="mt-2 text-sm leading-6 text-zinc-600">
					Guides the company vision and overall strategy.
				</p>
			</article>
			<article class="border-t border-zinc-200 py-5">
				<h3 class="font-semibold text-zinc-950">CTO</h3>
				<p class="mt-2 text-sm leading-6 text-zinc-600">
					Leads technical direction and engineering.
				</p>
			</article>
			<article class="border-t border-zinc-200 py-5">
				<h3 class="font-semibold text-zinc-950">QA</h3>
				<p class="mt-2 text-sm leading-6 text-zinc-600">
					Tests product workflows and helps maintain quality.
				</p>
			</article>
			<article class="border-t border-zinc-200 py-5">
				<h3 class="font-semibold text-zinc-950">Project Manager</h3>
				<p class="mt-2 text-sm leading-6 text-zinc-600">
					Coordinates priorities, timelines, and delivery.
				</p>
			</article>
		</div>
	</section>
</main>

<footer class="border-t border-zinc-200 px-24 py-12">
	<div class="grid grid-cols-1 gap-10 md:grid-cols-3">
		<div>
			<img
				src={Logo}
				class="size-8 rounded-sm"
				width="32"
				height="32"
				alt="Logo"
			/>
			<p class="mt-4 max-w-xs text-sm leading-6 text-zinc-600">
				Simple tools to help your team create and manage content.
			</p>
		</div>

		<nav aria-label="Footer navigation">
			<h2 class="font-semibold text-zinc-950">Explore</h2>
			<ul class="mt-4 space-y-3 text-sm text-zinc-600">
				<li>
					<a class="hover:text-zinc-950" href="#features">Features</a>
				</li>
				<li>
					<a class="hover:text-zinc-950" href="#pricing">Pricing</a>
				</li>
				<li><a class="hover:text-zinc-950" href="#faqs">FAQs</a></li>
			</ul>
		</nav>

		<div>
			<h2 class="font-semibold text-zinc-950">Get started</h2>
			<p class="mt-4 text-sm leading-6 text-zinc-600">
				Find the right plan for your next project.
			</p>
			<a
				class="mt-4 inline-flex font-medium text-zinc-950 underline underline-offset-4"
				href="#pricing"
			>
				View plans
			</a>
		</div>
	</div>
</footer>

<style>
	.feature-sprite {
		background-image: url("/kit.png");
		background-size: 400% 300%;
		background-position: var(--sprite-x) var(--sprite-y);
		background-repeat: no-repeat;
	}
</style>
