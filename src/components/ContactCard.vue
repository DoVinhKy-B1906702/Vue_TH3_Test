<script>
export default {
  props: {
    contact: { type: Object, required: true },
  },
};
</script>
<template>
  <div>
    <div class="p-1">
      <strong>Tên:</strong>
      {{ contact.name }}
    </div>
    <div class="p-1">
      <strong>E-mail:</strong>
      {{ contact.email }}
    </div>
    <div class="p-1">
      <strong>Địa chỉ:</strong>
      {{ contact.address }}
    </div>
    <div class="p-1">
      <strong>Điện thoại:</strong>
      {{ contact.phone }}
    </div>
    <div class="p-1">
      <strong>Liên hệ yêu thích:&nbsp;</strong>
      <span v-if="contact.favorite" class="v-check">V</span>
      <span v-else class="x-check" >X</span>
    </div>
  </div>
</template>
<style>
.v-check,.x-check {
  font-weight: 600;
  font-size: 1.2rem;
  border-radius : 50px;
  padding: 4px 12px;
}
.v-check {
  --color: green;
  color: var(--color);
  border: 1px solid var(--color);
}
.x-check {
  --color: red;
  color: var(--color);
  border: 1px solid var(--color);
}
</style>