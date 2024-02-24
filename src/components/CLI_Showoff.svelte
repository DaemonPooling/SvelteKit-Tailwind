<script>
	import Type from "../utils/Type.svelte";
</script>
<div id="Terminal" class="flex flex-col h-screen justify-between">
    <div id="Window_Bar" class="bg-white/5 w-full h-9 border-b border-b-white/5 flex items-center justify-between pl-3">
        <div id="Window_title" class="text-white font-mono text-shadow">Terminal</div>
        <div class="h-full">
            <button class="hover:bg-white/5 text-white w-12 h-full">—</button>
            <button class="hover:bg-white/5 text-white w-12 h-full">▢</button>
            <button class="hover:bg-red-500 text-white w-12 h-full">⨉</button>
          </div>
    </div>
    <div id="Console" class="w-full h-full flex-grow">
        <span>PS D:\Admin\web\intro ><Type text="HELLOO" duration=80 wait=2000/></span>
    </div>
</div>
<style>
    #Window_title {
        text-shadow: 0 0 15px #sfff;
    }
</style>