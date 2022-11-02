<template>
  <div class="page">
    <h4>Hiệu chỉnh Liên hệ</h4>
    <CreateForm :contact="contact" @add:contact="createContact" />
    <p>{{ message }}</p>
  </div>
</template>
<script>
import CreateForm from '@/components/CreateForm.vue';

import ContactService from '@/services/contact.service';
export default {
  components: {
    CreateForm,
  },
  data() {
    return {
      contact: { name },
      message: '',
    };
  },
  methods: {
    async createContact(data) {
      try {
        await ContactService.create(data);
        this.message = 'Liên hệ được thêm thành công.';
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>
