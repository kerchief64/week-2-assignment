<script>
    import MyButton from "./MyButton.svelte";

    function say_hi() {
        alert("hi there!")
    }
    
</script>

<!-- 
    Change the internals of MyButton so that `text="Login"` works
    (The button should say "Login")
-->
<MyButton text="Login"></MyButton>

<!-- 
    Change the internals of MyButton so that if `text` isn't specified, the button displays "Send" by default
-->
<MyButton></MyButton>

<!-- 
    Change the onclick behavior of this button by using the `click_event` property as a proxy
    The function `say_hi()` from above should instead be used

    Note: You could struggle with this one. If you can't figure it out after an hour move on and we will go over it together
 -->
<MyButton click_event={say_hi} text="Say Hi"></MyButton>