<h4>Tell Us About Yourself</h4>

<p>Hello {fullName},</p>
<form action="">
    <div>
        <label for="firstName">First Name</label>
        <input type="text" id="firstName" bind:value="{firstName}">
    </div>

    <div>
        <label for="lastName">Last Name</label>
        <input type="text" id="lastName" bind:value="{lastName}">
    </div>
</form>

<script>
    let firstName = '';
    let lastName = ''

    $: fullName = `${firstName} ${lastName}`
</script>