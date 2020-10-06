<template>
    <form name="ask-question" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
        <input type="hidden" name="form-name" value="ask-question" />
      <p>
        <label> <input type="hidden" name="form-name" value="simple-form" /></label>   
      </p>
      <p>
        <label>Your Name: <input type="text" name="name" /></label>   
      </p>
      <p>
        <label>Your Email: <input type="email" name="email" /></label>
      </p>
      <p>
        <label>Message: <textarea name="message"></textarea></label>
      </p>
      <p>
        <button type="submit">Send</button>
      </p>
    </form>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

</style>