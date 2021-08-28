<script>
    let darkMode = false
    let num = 1

    function toggleTheme() {
        if (darkMode) {
            document.body.classList.remove("darkMode")
        } else {
            document.body.classList.add("darkMode")
        }
        
        darkMode = !darkMode
    }
</script>


<div on:click={toggleTheme}>
    {darkMode ? "🌑" : "🌞"}
</div>


<style>
    :global(body) {
        background: rgb(255, 255, 255);
        transition: 1s;
    }  
    :global(body.darkMode) {
        background: black;
    }
    :global(body.darkMode h1) {
        color: white !important;
    }
    :global(body.darkMode img) {
        filter: invert(2) !important;
    }
    div {
        cursor: pointer;
        width: max-content;
    }
</style>