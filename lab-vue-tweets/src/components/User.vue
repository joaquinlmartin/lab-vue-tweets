<template>
    <div>
    <span class="name">{{ user.name }}</span>
    <span class="handle">{{ user.handle }}</span>
    </div>
</template>

<script>
export default {
  name: 'User',
  props: {
    user: {
      name: String,
      handle: String,
    },
  },
};
</script>
