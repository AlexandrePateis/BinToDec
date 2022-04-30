<template>
    <div class="paragrafo">
        <p class="title">A bit of history...</p>
        <p>
            Binary-coded decimal and/or binary encoding, also known as BCD (Binary-coded decimal), is a numbering system widely used in Computer Science, as well as in Mathematics, and in electronic digital systems. We are talking about a base two and positional system, that is, changing the order of the digits in the binary number, its value is changed. It uses only two digits: 0 (zero) and 1 (one).[1] BCD encodes the decimal system in binary, from (decimal) numbers 0 to 9, where each number is represented by its binary equivalent.
        </p>
    </div>
</template>

<script>
export default {
    name:"History"
}
</script>

<style scoped>
p{
    width: 100%;
    display: inlin-block;
    color: white;
    @import url('https://fonts.googleapis.com/css2?family=Acme&display=swap');
    font-family: 'Acme', sans-serif;
    line-height: 1.5em;
}
.paragrafo{
    
    width: 30%;
}
.title{
    font-size: 2em;
}
</style>