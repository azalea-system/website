<script lang="ts">
	import { Button } from '$lib/components/ui/button/index.js';
	import ServerIcon from '@iconify-svelte/pixelarticons/server';
	import CloudServerIcon from '@iconify-svelte/pixelarticons/cloud-server';
	import MusicIcon from '@iconify-svelte/pixelarticons/music';
	import DownloadIcon from '@iconify-svelte/pixelarticons/download';
	import GamepadIcon from '@iconify-svelte/pixelarticons/gamepad';
	import LaughIcon from '@iconify-svelte/pixelarticons/laugh';
	import ChatIcon from '@iconify-svelte/pixelarticons/chat';
</script>

<section>
	<div class="flex flex-col">
		<h1 class="p-0 m-0 h-28">Azalea<span class="font-[Inter] text-sm ml-2 text-yellow-600">alpha</span></h1>
		<p class="pixel text-[1.5rem]!">is the <b>media server</b> that <b>cares</b>.</p>
	</div>
	<ul class="mb-2 mt-1 *:flex *:*:w-5 *:gap-1">
		<li><ServerIcon />Self-Hosted</li>
		<li><CloudServerIcon />Online Integration</li>
		<li><MusicIcon />Works with most media</li>
		<li>
			<LaughIcon />Licensed under <a href="https://www.gnu.org/licenses/gpl-3.0.en.html">GPLv3</a>
		</li>
	</ul>
	<div class="flex gap-2 *:h-14 *:p-4 *:text-[1.3em]">
		<Button
			href="https://github.com/azalea-system/azalea/releases/latest/download/azalea-windows-x86_64-installer.exe"
			><DownloadIcon class="size-5" />Download Latest</Button
		>
		<Button
			href="https://azalea-web.vercel.app"
			target="_blank"
			class="bg-neutral-50 text-neutral-900 hover:bg-neutral-200!"
			><GamepadIcon class="size-5" />Online Demo</Button
		>
	</div>
	<div>
		<a href="https://github.com/azalea-system/azalea/releases" class="text-md">see all versions...</a>
	</div>
</section>

<section class="gap-8!">
    <div>
    	<h2>Why?</h2>
    	<p>
    		Azalea <b>liberates</b> your media with fully <b>free & open-source</b> client apps which are <b>packed
    		full of features</b> - and no <a href="https://en.wiktionary.org/wiki/anti-feature#Noun"
    			>anti-features</a
    		>.
    	</p>
    </div>
    <div>
        <h2>How?</h2>
        <p>One of your computers hosts an Azalea server and then (by default) any other computer on your network can access Azalea through a web client which can be hosted alongside the server, or through a different client app.</p>
    </div>
    <div>
    	<h2>Where?</h2>
    	<p>Azalea runs on <b>your computer</b>, not in <b>the cloud</b>. It fetches data from the internet to <b>classify</b> your collection and <b>enrich</b> your experience with features such as <b>synced lyrics</b>, but this data is fully stored on <b>your computer</b> after fetch and Azalea can be used <b>offline</b> too.</p>
    </div>
    <div>
        <h2>What... am I downloading?</h2>
        <p>The big blue button downloads the Azalea server installer, which when run will give you the option to also install Azalea Web and Azalea Bridge.</p>
    </div>
    <div>
        <h2>Azalea Bridge?</h2>
        <p>It's just a small native tray app which helps you view logs, configure Azalea, and forward Discord presence. It can be hosted on any graphical machine. A CLI/service mode may be included in the future</p>
    </div>
</section>

<section class="border-2 border-accent bg-blue-200 p-8 items-center justify-center flex flex-col gap-10!">
    <h2>Connect</h2>
    <Button class="h-15 text-xl" href="https://matrix.to/#/#azaleasystem:matrix.org"><ChatIcon />Join the Matrix Room</Button>
</section>
