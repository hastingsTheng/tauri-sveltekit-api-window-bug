<script>
    import {WebviewWindow} from '@tauri-apps/api/window'
    import {open} from '@tauri-apps/api/shell'

    function createWebviewWindow() {
        const webview = new WebviewWindow('PopupWindow', {
            url: '/dialogs/popup',
            width: 400,
            height: 300,
            title: "Example Dialog"
        })
    }
</script>

<div id="test-component">
    <h3>Test Component</h3>
    <p>
        This is a test component.
        You could use test components to do all kinds of things.
        Inset UI panels, pop-up modal windows, 3D rendering, 2D plotting, Subprocesses - the possibilities are endless.
    </p>

    <div on:click={createWebviewWindow}>
        <a href='#'>Click me to open a dialog</a>
    </div>

    <p>
        Just like this component, we could make another component using <a href="#" on:click={() => {open('https://threejs.org/')}}>Three.js</a> to do our CAD rendering in an embeddable Svelte element 🤔
        It has built in IFC and DXF support.
        We could also use <a href="#" on:click={() => {open('https://speckle.systems/')}}>Speckle</a> to handle the management of our CAD data, allowing us to play nicer with third-party apps, and our own future apps. 
    </p>
</div>