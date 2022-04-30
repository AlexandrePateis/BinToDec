<template>
    <div class="main">
        <p class="paragrafo-principal">Instructions for use</p>
            <ol>
                <li>When starting, the program will always default to decimal to binary.</li>
                <li>To reverse the operation, simply click "Revert"</li>
                <li>If the option is from binary to decimal, only "0" and "1" will be accepted</li>
                <li>Finally, just click "Convert" to get the result.</li>
            </ol>
        </div>
</template>

<script>
    export default{
        name: "Instructions"
    }
</script>
<style scoped>
*{

    @import url('https://fonts.googleapis.com/css2?family=Acme&display=swap');
    font-family: 'Acme', sans-serif;
}
.main{
    width: 33%;
}
.paragrafo-principal{
    text-align: center;
    color: white;
    font-size: 2em;
}
li{
    color: white;
    line-height: 1.5em;
}
</style>