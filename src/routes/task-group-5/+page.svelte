<script>

    async function get_kitten() {

        let width = Math.floor(Math.random() * 800) + 100;
        let height = Math.floor(Math.random() * 800) + 100;

        let fakeFail = Math.floor(Math.random() * 2);
        console.log(`Fake Fail: ${fakeFail}`)

        let response_url = ""

        if (!fakeFail) {
            response_url = `https://placekitten.com/${width}/${height}`
        }

        const response = await fetch(response_url)
        
        const blob = await response.blob()

        const url = URL.createObjectURL(blob.slice(0, 4000))

        return url
    }
    
    function handleClick() {
		kitten = get_kitten();
	}

    let kitten = get_kitten()
</script>


<!-- This button (when setup correctly) will grab a random image from the "Place Kitten" Public API https://placekitten.com/ -->
<!-- The button has a 50% change to fail to simulate an error happening -->
<button on:click={handleClick}>
	Generate Random Cat
</button>

<br><br>

<!-- Fix the syntax below and make the kitten images load and the error message display if failed-->
<!-- {await kitten} -->
	<p>...waiting</p>
<!-- {:then url} -->
	<img src="" alt="Kitten">
<!-- {#catch error -->
	<p style="color: red">error.message</p>
<!-- {await} -->