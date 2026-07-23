<script lang="ts">
	type NavItem = {
		label: string;
		newTab?: boolean;
		dropdown?: {
			width: string;
			items: { title: string; href: string; desc: string }[];
		};
		href?: string;
	};

	const navItems: NavItem[] = [
		{
			label: 'Home',
			href: "/website"
		},
		{
			label: 'Code',
			newTab: true,
			dropdown: {
				width: 'w-[400px]',
				items: [
					{ title: 'Main GitHub Page', href: 'https://github.com/azalea-system', desc: 'The overarching GitHub page for the other repos.' },
					{ title: 'Azalea', href: 'https://github.com/azalea-system/azalea', desc: 'The official azalea server implementation.' },
					{ title: 'Azalea Web', href: 'https://github.com/azalea-system/azalea-web', desc: 'A nice web UI for azalea, usually bundled in.' },
					{ title: 'Azalea Bridge', href: 'https://github.com/azalea-system/azalea-bridge', desc: 'A remote control and media agent for the azalea server.' }
				]
			}
		},
		{
			label: 'About',
			href: 'about'
		}
	];
</script>

<nav class="flex items-center gap-1">
	{#each navItems as item}
		{#if item.dropdown}
			<details class="group relative">
				<summary
					class="cursor-pointer list-none rounded-md px-3 py-2 text-md hover:bg-accent hover:text-accent-foreground font-bold"
				>
					{item.label}
					<span class="ml-1 inline-block transition-transform group-open:rotate-180">▾</span>
				</summary>
				<div
					class="absolute left-0 z-50 mt-1 rounded-md border bg-popover p-2 text-popover-foreground shadow-md {item.dropdown.width}"
				>
					<ul class="grid gap-1">
						{#each item.dropdown.items as link}
							<li>
								<a
									href={link.href}
									target={item.newTab ? '_blank' : '_self'}
									class="block rounded-md p-3 no-underline hover:bg-neutral-200 hover:border-accent border-3"
								>
									<div class="text-md font-bold">{link.title}</div>
									<p class="line-clamp-2 text-xs text-muted-foreground font-[Inter]">{link.desc}</p>
								</a>
							</li>
						{/each}
					</ul>
				</div>
			</details>
		{:else}
			<a
				href={item.href}
				class="rounded-md px-3 py-2 text-md no-underline hover:bg-accent hover:text-accent-foreground! font-bold"
			>
				{item.label}
			</a>
		{/if}
	{/each}
</nav>

<style>
	details[open] > summary::after {
		content: '';
		position: fixed;
		inset: 0;
		z-index: 40;
	}

	a {
		text-decoration: inherit;
		color: inherit;
	}

	summary,
	a {
		font-family: "Noto Serif";
		user-select: none;
	}
</style>
