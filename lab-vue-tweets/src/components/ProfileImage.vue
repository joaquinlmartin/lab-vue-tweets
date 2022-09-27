<template>
    <div>
        <img :src="image" class="profile" alt="profile"/>
    </div>
</template>

<script>
export default {
  name: 'ProfileImage',
  props: {
    image: String,
  },
};
</script>
