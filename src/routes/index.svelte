<script>
    import { WebviewWindow } from "@tauri-apps/api/window";

    function createWindow() {
        //From: https://github.com/tauri-apps/tauri/blob/dev/examples/api/src/components/Window.svelte
        const label = Math.random().toString().replace('.', '')
        const webview = new WebviewWindow(
            label,
            {
                url: 'https://google.com'
            }
        )    
    }
</script>

<div>
    <a on:click={() => createWindow} href="#">Click me to spawn a WebViewWindow</a>
</div>