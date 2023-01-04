<script>
    let programmingLanguages = [
        { name: "Python", executionType: "interpreted", speed: "slow", difficulty: "easy"},
        { name: "JavaScript", executionType: "interpreted", speed: "lower average", difficulty: "Medium"},
        { name: "C++", executionType: "Compiled", speed: "very fast", difficulty: "Hard"},
        { name: "C#", executionType: "JIT Compiled", speed: "average", difficulty: "Medium"},
        { name: "Rust", executionType: "Compiled", speed: "very fast", difficulty: "Extremely Hard"},
        { name: "Assembly Language", executionType: "Compiled", speed: "fastest possible", difficulty: "Gigga Brain Chad"},
    ]
</script>

<h1>Programming Languages</h1>
<ul>
    <li>Python: interpreted, slow, easy</li>
    <li>JavaScript: interpreted, lower average, Medium</li>
    <li>C++: Compiled, very fast, Hard</li>
    <li>C#: JIT Compiled, average, Medium</li>
    <li>Rust: Compiled, very fast, Extremely Hard</li>
    <li>Assembly Language: Compiled, fastest possible, Gigga Brain Chad</li>
</ul>

<br><br>

<h1>Programming Languages</h1>
<ul>
    <!-- Fix this argument based each block. It should look like the original at the top -->
    <!-- {!eac programmingLanguages as {name, executionType, difficulty} } -->
        <!-- <li>{name}: {executionType}, {speed}, {difficulty}</li> -->
    <!-- {#each} -->
</ul>

<br><br>

<h1>Programming Languages</h1>
<ul>
    <!-- Fix this object based each block. It should look like the original at the top -->
    <!-- {#each programmingLanguage in language } -->
        <!-- <li>{language.name}: {language.speed}, {language.dificulty}</li> -->
    <!-- {/each} -->
</ul>