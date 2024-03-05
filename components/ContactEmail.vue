<template>

  <form @submit.prevent="handleSubmit()" class="form-floating needs-validation row px-5" novalidate>

    <div class="col-6 mb-3 ">
      <div class="form-floating has-validation">
        <input type="text" class="form-control " id="name" placeholder="Name" v-model="form.name">
        <label for="name" class="ms-2">Name</label>
        <div class="invalid-feedback">please fill out name</div>
      </div>
    </div>

    <div class="col-6 mb-3 form-floating">
      <input type="email" class="form-control is-valid" id="email" placeholder="Email" v-model="form.email">
      <label for="email" class="ms-2">Email</label>

    </div>
    <div class="col-12 mb-5 form-floating">
      <input type="text" class="form-control " id="subject" placeholder="Subject" v-model="form.subject">
      <label class="ms-2" for="subject">Subject</label>
    </div>
    <div class="col-12 mb-5 form-floating">
      <textarea class="form-control message" placeholder="Leave a comment here" id="floatingTextarea"></textarea>
      <label for="floatingTextarea" class="ms-2">Message</label>
    </div>

    <div class="col-12">
      <button class="btn btn-primary" type="submit">Send Email</button>
    </div>

  </form>

</template>


<script>
import { computed, onMounted, ref } from 'vue';

export default {
  setup() {
    const form = ref({})
    return {
      form,
      handleSubmit() {
        console.log('does this work');
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.message {
  width: 100%;
  min-height: 25vh;
}
</style>

