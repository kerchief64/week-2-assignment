<script>
    import { error } from '@sveltejs/kit';


    class UserPermissions {
        static admin() {
            return "ADMIN"
        }

        static guest() {
            return "GUEST"
        }

        static isValid(value) {
            let validValues = [this.guest(), this.admin()];

            if (validValues.indexOf(value) > -1) return true
            else return false
        }
    }

    class User {
        constructor(name, permissions) {
            if (!UserPermissions.isValid(permissions)) {
                throw error(500, {
                    message: `Invalid permission given: '${permissions}'`
                });
            }
            this.permissions = permissions
            this.name = name;
        }
    }

    let x = 5

    // let user = new User("Joe", UserPermissions.guest())
    let user = new User("Jeffery", UserPermissions.guest())

</script>

<p>User Name: {user.name}</p>
<p>User Permissions: {user.permissions}</p>

<!-- Challenge: Get rid of all the <p>failed</p> elements without deleting or modifying them -->

<!-- Uncomment and fix the syntax below to get rid of the failed element -->
{#if x!==5}
    <p>failed</p>
{/if}


<!-- 
    Fix the syntax, but do not change the main equations. 
    Instead, replace the failed elements with a success element by changing the "user" variable in the <script> above
-->
{#if user.name === "Joe"}
    <p>Failed</p>
{:else if user.name === "Jeffery"}
    <p>Success</p>
{:else}
    <p>Failed</p>
{/if}

<!-- 
    Create a svelte if block around the failed element below to hide it. 
    You may do this in a couple different ways, but use the x variable (unchanged) to do it 
-->
{#if x === Symbol }
    <p>Failed</p>
{/if}
