<script lang="ts">
    import { clickOutside } from "$lib/helpers"
    import "../styles/main.scss"

    let expandSidebar = true
    let open = false

    function toggleExpandSidebar() {
        if (expandSidebar) {
            localStorage.setItem("blueLayoutShrinkSidebar", "true")
        } else {
            localStorage.removeItem("blueLayoutShrinkSidebar")
        }
        expandSidebar = !expandSidebar
    }
</script>

<main class="blue-layout hasSidebarMenu" class:expandSidebar class:open>
    <div class="blue-sidebar-toggler blue-tooltip-end position-fixed" data-tooltip="Menü umschalten">
        <button
            type="button"
            class="blue-open-menu blue-menu-item btn rounded-0"
            aria-label="Menü umschalten"
            on:click={() => {
                open = !open
            }}
            ><div class="blue-sidebar-exception position-absolute w-100 h-100" />
            <svg
                xmlns="http://www.w3.org/2000/svg"
                width="1em"
                height="1em"
                fill="currentColor"
                viewBox="0 0 16 16"
                style="display: inline-block; vertical-align: -0.125em;"
                ><path
                    fill-rule="evenodd"
                    d="M2.5 12a.5.5 0 01.5-.5h10a.5.5 0 010 1H3a.5.5 0 01-.5-.5zm0-4a.5.5 0 01.5-.5h10a.5.5 0 010 1H3a.5.5 0 01-.5-.5zm0-4a.5.5 0 01.5-.5h10a.5.5 0 010 1H3a.5.5 0 01-.5-.5z"
                /></svg
            ></button
        >
    </div>

    <div class="blue-sidebar-toggler blue-tooltip-end position-fixed d-none d-xxl-block" data-tooltip="Menü umschalten">
        <button
            type="button"
            class="blue-open-menu blue-menu-item btn rounded-0"
            aria-label="Menü umschalten"
            on:click={toggleExpandSidebar}
            ><div class="blue-sidebar-exception position-absolute w-100 h-100" />
            <svg
                xmlns="http://www.w3.org/2000/svg"
                width="1em"
                height="1em"
                fill="currentColor"
                viewBox="0 0 16 16"
                style="display: inline-block; vertical-align: -0.125em;"
                ><path
                    fill-rule="evenodd"
                    d="M2.5 12a.5.5 0 01.5-.5h10a.5.5 0 010 1H3a.5.5 0 01-.5-.5zm0-4a.5.5 0 01.5-.5h10a.5.5 0 010 1H3a.5.5 0 01-.5-.5zm0-4a.5.5 0 01.5-.5h10a.5.5 0 010 1H3a.5.5 0 01-.5-.5z"
                /></svg
            ></button
        >
    </div>

    <div class="blue-sidebar overflow-visible">
        <div class="blue-sidebar-top">
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Search">
                <form class="blue-search blue-search-sidebar blue-sidebar-visible-on-open undefined">
                    <div class="blue-search-input-group input-group">
                        <span class="input-group-text"
                            ><span
                                ><svg
                                    width="1em"
                                    height="1em"
                                    viewBox="0 0 16 16"
                                    class="bi bi-search mt-n1"
                                    fill="currentColor"
                                    xmlns="http://www.w3.org/2000/svg"
                                    ><path
                                        fill-rule="evenodd"
                                        d="M10.442 10.442a1 1 0 0 1 1.415 0l3.85 3.85a1 1 0 0 1-1.414 1.415l-3.85-3.85a1 1 0 0 1 0-1.415z"
                                    /><path
                                        fill-rule="evenodd"
                                        d="M6.5 12a5.5 5.5 0 1 0 0-11 5.5 5.5 0 0 0 0 11zM13 6.5a6.5 6.5 0 1 1-13 0 6.5 6.5 0 0 1 13 0z"
                                    /></svg
                                ></span
                            ></span
                        ><input
                            type="search"
                            id="blue-search-control-2abb4d8a-2539-f775-acf7-f706093ae539"
                            class="blue-search-control form-control default input-lg"
                            placeholder="Search in menu"
                            value=""
                        />
                    </div>
                </form>
                <button class="blue-menu-item btn blue-search-btn"
                    ><span class="blue-menu-item-icon"
                        ><span
                            ><svg
                                width="1em"
                                height="1em"
                                viewBox="0 0 16 16"
                                class="bi bi-search mt-n1"
                                fill="currentColor"
                                xmlns="http://www.w3.org/2000/svg"
                                ><path
                                    fill-rule="evenodd"
                                    d="M10.442 10.442a1 1 0 0 1 1.415 0l3.85 3.85a1 1 0 0 1-1.414 1.415l-3.85-3.85a1 1 0 0 1 0-1.415z"
                                /><path
                                    fill-rule="evenodd"
                                    d="M6.5 12a5.5 5.5 0 1 0 0-11 5.5 5.5 0 0 0 0 11zM13 6.5a6.5 6.5 0 1 1-13 0 6.5 6.5 0 0 1 13 0z"
                                /></svg
                            ></span
                        ></span
                    ></button
                >
            </div>
        </div>
        <div
            class="blue-menu overflow-visible"
            use:clickOutside
            on:outclick={() => {
                open = false
            }}
        >
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Home">
                <a href="#home" class="blue-menu-item btn active has-label"
                    ><span class="blue-menu-item-icon"
                        ><svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 16 16"
                            width="1em"
                            height="1em"
                            fill="currentColor"
                            class="bi"
                            ><path
                                fill-rule="evenodd"
                                d="M2 13.5V7h1v6.5a.5.5 0 0 0 .5.5h9a.5.5 0 0 0 .5-.5V7h1v6.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 13.5zm11-11V6l-2-2V2.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5z"
                            /><path
                                fill-rule="evenodd"
                                d="M7.293 1.5a1 1 0 0 1 1.414 0l6.647 6.646a.5.5 0 0 1-.708.708L8 2.207 1.354 8.854a.5.5 0 1 1-.708-.708L7.293 1.5z"
                            /></svg
                        ></span
                    ><span class="blue-menu-item-label text-truncate">Home</span></a
                >
            </div>
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Documents">
                <button class="blue-menu-item btn blue-menu-item-dropdown-toggle has-label"
                    ><span class="blue-menu-item-icon"
                        ><svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 16 16"
                            width="1em"
                            height="1em"
                            fill="currentColor"
                            class="bi"
                            ><path
                                d="M14 4.5V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2h5.5L14 4.5zm-3 0A1.5 1.5 0 0 1 9.5 3V1H4a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V4.5h-2z"
                            /></svg
                        ></span
                    ><span class="blue-menu-item-label text-truncate">Documents</span><span
                        class="blue-caret blue-caret-mirrored blue-menu-item-dropdown-caret mt-2"
                    /></button
                >
            </div>
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Appointments">
                <button class="blue-menu-item btn has-label"
                    ><span class="blue-menu-item-icon"
                        ><svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 16 16"
                            width="1em"
                            height="1em"
                            fill="currentColor"
                            class="bi"
                            ><path
                                d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4H1z"
                            /></svg
                        ></span
                    ><span class="blue-menu-item-label text-truncate">Appointments</span></button
                >
            </div>
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Users">
                <button class="blue-menu-item btn has-label"
                    ><span class="blue-menu-item-icon"
                        ><svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 16 16"
                            width="1em"
                            height="1em"
                            fill="currentColor"
                            class="bi"
                            ><path
                                d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0zm4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4zm-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10c-2.29 0-3.516.68-4.168 1.332-.678.678-.83 1.418-.832 1.664h10z"
                            /></svg
                        ></span
                    ><span class="blue-menu-item-label text-truncate">Users</span></button
                >
            </div>
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Hello World" title="">
                <button class="blue-menu-item btn has-label"
                    ><span class="blue-menu-item-icon"><span>😅</span></span><span
                        class="blue-menu-item-label text-truncate">Hello World</span
                    ></button
                >
            </div>
        </div>
        <div class="blue-sidebar-bottom">
            <div class="blue-tooltip-end blue-sidebar-pseudo-hidden-on-open" data-tooltip="Sign out">
                <a href="#intro" class="blue-menu-item btn has-label"
                    ><span class="blue-menu-item-icon"
                        ><svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 16 16"
                            width="1em"
                            height="1em"
                            fill="currentColor"
                            class="bi"
                            ><path
                                fill-rule="evenodd"
                                d="M6 12.5a.5.5 0 0 0 .5.5h8a.5.5 0 0 0 .5-.5v-9a.5.5 0 0 0-.5-.5h-8a.5.5 0 0 0-.5.5v2a.5.5 0 0 1-1 0v-2A1.5 1.5 0 0 1 6.5 2h8A1.5 1.5 0 0 1 16 3.5v9a1.5 1.5 0 0 1-1.5 1.5h-8A1.5 1.5 0 0 1 5 12.5v-2a.5.5 0 0 1 1 0v2z"
                            /><path
                                fill-rule="evenodd"
                                d="M.146 8.354a.5.5 0 0 1 0-.708l3-3a.5.5 0 1 1 .708.708L1.707 7.5H10.5a.5.5 0 0 1 0 1H1.707l2.147 2.146a.5.5 0 0 1-.708.708l-3-3z"
                            /></svg
                        ></span
                    ><span class="blue-menu-item-label text-truncate">Sign out</span></a
                >
            </div>
        </div>
    </div>

    <div class="router-page active">
        <slot />
    </div>
</main>
