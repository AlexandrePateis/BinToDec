<template>
    <div class="footer">
        <p>Alexandre Pateis</p>
        <ul>
            <li><a href="https://www.instagram.com/alexandrepateis/" target="_blank"><i class="fa-brands fa-instagram"></i></a></li>
            <li><a href="https://github.com/AlexandrePateis" target="_blank"><i class="fa-brands fa-github-square"></i></a></li>
            <li><a href="www.linkedin.com/in/alexandre-pateis" target="_blank"><i class="fa-brands fa-linkedin"></i></a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name:"Footer"
}
</script>

<style scoped>
*{
    color:white;
}
p{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-size: 1.2em;
}
ul{
    list-style: none;
    align-items: center;
    display: flex;
    font-size: 2em;
    gap: 1em;
    justify-content: center;
    padding: 0 !important;
}
.footer{
    justify-content: center;
    flex-direction: column;
    align-items: center;
    margin-top: 18em;
}
</style>