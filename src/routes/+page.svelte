<svelte:head>
    <title>Welcome to Blue Svelte!</title>
</svelte:head>

<header class="blue-header">
    <div class="h3 blue-header-logo">
        <span class="blue-header-logo-title">
            <a href="/"
                ><img
                    alt="Logo"
                    class="blue-header-logo-image"
                    src="https://bruegmann.github.io/blue-react/v9/static/media/blue.fb422456b614ac039838a6847b7f8a97.svg"
                /></a
            >
            <span class="blue-header-logo-title-labels keep"><a href="/">Blue Svelte</a></span>
        </span>
    </div>

    <div class="blue-actions none">
        <nav class="blue-actions-menu float-end d-flex">
            <a href="/" class="blue-menu-item btn active" aria-current="page">
                <span class="blue-menu-item-icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="1em"
                        height="1em"
                        fill="currentColor"
                        class="bi bi-chat-left-heart-fill"
                        viewBox="0 0 16 16"
                    >
                        <path
                            d="M2 0a2 2 0 0 0-2 2v12.793a.5.5 0 0 0 .854.353l2.853-2.853A1 1 0 0 1 4.414 12H14a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2H2Zm6 3.993c1.664-1.711 5.825 1.283 0 5.132-5.825-3.85-1.664-6.843 0-5.132Z"
                        />
                    </svg></span
                >
                <span class="blue-menu-item-label text-truncate">Posts</span>
            </a>

            <button
                class="blue-menu-item btn"
                on:click={() => {
                    localStorage.removeItem("currentUser")
                    location.reload()
                }}
            >
                <span class="blue-menu-item-icon"
                    ><svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="1em"
                        height="1em"
                        fill="currentColor"
                        class="bi bi-box-arrow-left"
                        viewBox="0 0 16 16"
                    >
                        <path
                            fill-rule="evenodd"
                            d="M6 12.5a.5.5 0 0 0 .5.5h8a.5.5 0 0 0 .5-.5v-9a.5.5 0 0 0-.5-.5h-8a.5.5 0 0 0-.5.5v2a.5.5 0 0 1-1 0v-2A1.5 1.5 0 0 1 6.5 2h8A1.5 1.5 0 0 1 16 3.5v9a1.5 1.5 0 0 1-1.5 1.5h-8A1.5 1.5 0 0 1 5 12.5v-2a.5.5 0 0 1 1 0v2z"
                        />
                        <path
                            fill-rule="evenodd"
                            d="M.146 8.354a.5.5 0 0 1 0-.708l3-3a.5.5 0 1 1 .708.708L1.707 7.5H10.5a.5.5 0 0 1 0 1H1.707l2.147 2.146a.5.5 0 0 1-.708.708l-3-3z"
                        />
                    </svg></span
                >
                <span class="blue-menu-item-label text-truncate">Logout</span>
            </button>
        </nav>
    </div>
</header>

<div class="blue-page bg-body py-4">
    <div class="container">
        <img src="/favicon.png" alt="Svelte Logo" />
        <h1>Welcome to SvelteKit</h1>
        <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

        <p>
            This site is built with SvelteKit and uses stylesheets from <a href="https://bruegmann.github.io/blue-react"
                >Blue React</a
            >.
        </p>
    </div>
</div>
