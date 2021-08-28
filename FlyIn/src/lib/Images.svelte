<script>
    const images = [
        "/Angry.jpg",
        "/Boy.webp",
        "/Bunny.jpg",
        "/Foxy.png",
        "/Golden.jpg",
        "/Chica.jpg"
    ]

    let centerImage = false, showPrice = []

    function random() {
        return Math.floor(Math.random() * 200 - 100)
    }

    setTimeout(() => {
        centerImage = true
    }, 100);
</script>

    <div class="container">

        {#each images as image, i}
                <div class="box">

                <img class:center={centerImage} style="transform: translate({random()}px, {random()}px);" src={image} alt="">
                
                <button on:click={() => showPrice[i] = !showPrice[i]}>
                    {#if showPrice[i]}
                        ${Math.abs(random()) * 65452}
                    {:else}
                        Show Price
                    {/if}
                </button>
                
            </div>

        {/each}

    </div>

<style>
    img {
        width: 150px;
        height: auto;
        margin: auto;
        border-radius: 25px;
        transition: 2s;
        filter: brightness(1.1)
    }
    .center {
        transform: translate(0,0) !important;
    }
    .container {
        display: grid;

        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;

        gap: 2rem 10rem;
        max-width: min(800px, 95vw);
        margin: 2rem auto;
    }
    .box {
        border: 5px inset gray;
        border-radius: 25px;
        padding: 10px;
        align-items: center;
        display: flex;
        flex-direction: column;
    }
    button {
        background: transparent;
        color: gray;
        font-family: 'IBM Plex Sans KR', sans-serif;
        letter-spacing: 3px;
        text-transform: uppercase;
    }
</style>