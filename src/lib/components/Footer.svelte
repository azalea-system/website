<script lang="ts">
    let currentYear = new Date().getFullYear();
</script>

<footer class="p-2 py-10 bg-black text-white flex justify-center w-full">
    <div class="flex gap-15 *:flex *:flex-col *:gap-2">
        <section>
            <span><span class="font-sans">&copy;</span> {currentYear} Ethan Martin</span>
            <span>Licensed under the GPLv3</span>
        </section>
        <section>
            <span>Repositories</span>
            <a href="https://github.com/azalea-system/azalea">Azalea Server</a>
            <a href="https://github.com/azalea-system/azalea-web">Azalea Web</a>
            <a href="https://github.com/azalea-system/azalea-bridge">Azalea Bridge</a>
        </section>
        <section>
            <span>Links</span>
            <a href="https://github.com/azalea-system">GitHub</a>
            <a href="https://matrix.to/#/#azaleasystem:matrix.org">Matrix Room</a>
        </section>
        <section>
            <span>Related Projects</span>
            <a href="https://opensubsonic.netlify.app/docs/">OpenSubsonic</a>
            <a href="https://github.com/yt-dlp/yt-dlp">yt-dlp</a>
        </section>
        <section>

        </section>
    </div>
</footer>

<style>
    a {
        color: gray;
    }
</style>
