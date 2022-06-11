<script>
    import {open} from '@tauri-apps/api/shell'
</script>

<div>
    <h1>Welcome to Burning Argon</h1>
    <div id="intro-section">
        <h2>Introduction</h2>
        <div>

            <h3>Frameworks</h3>

            <p>This application is built with the following frameworks.</p>
            
            <h4 on:click={async () => await open('https://tauri.studio')}>Tauri</h4>
            <p>
                Tauri is a framework that allows you to use web development languages and frameworks to develop native applications, but it is built on Rust and native webviews so it is not memory hungry and 💩 like Electron.
            </p>

            <h4 on:click={async () => await open('https://svelte.dev')}>Svelte</h4>
            <p>
                Svelte is a JS compiler that builds lightning fast applications from your JS source code, rather than relying on the client and browser to render JS at runtime like React.
            </p>

            <h4 on:click={async () => await open('https://kit.svelte.dev')}>Svelte Kit</h4>
            <p>
                Sveltekit is a framework for Svelte applications.
                It is not doing a whole lot that I can see for the final deployed application, however in development, it provides a live reloading development server for your front end through Tauri, allowing you to make real-time changes without having to wait on a build.
            </p>

            <h4 on:click={async () => await open('https://tailwindcss.com')}>TailwindCSS</h4>
            <p>
                TailwindCSS is a framework for styling webapps.
                This isn't technically installed in this app, but it could very easily be.
                I just didn't take the time to set it up.
            </p>

            <h3>Languages</h3>
            <h4>Frontend</h4>
            <p>
                The UI in this app uses JS, HTML, and CSS in the Sveltekit framework to pre-render static HTML pages at build time, that are then displayed in the Webview by Tauri at run time.
                Tauri is able to display the same UI across all different platforms by using the platform's native webview (Example: This Windows app uses the new Webview2).
            </p>
            <h4>Backend</h4>
            <p>
                The backend of the app is written using Rust.
                It is isolated from the front-end by Tauri, and is only accessible via routes defined in the source code and created at build time.
                The backend handles all access to system resources at runtime, so this configuration guards against malicious entities using the Javascript-enabled WebView Frontend to access system resources, such as filesystem or networking tools.
            </p>
        </div>
    </div>

    <a href="/test">Next window</a>
</div>
