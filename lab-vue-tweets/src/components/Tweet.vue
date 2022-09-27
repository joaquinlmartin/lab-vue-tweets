<template>
  <div class="tweet">
    <ProfileImage :image="image"/>
    <div class="body">
      <div class="top">
        <span class="user">
          <User :user="user"/>
        </span>
        <Timestamp :timestamp ="timestamp"/>
      </div>
      <Message :message="message"/>
      <Actions/>
    </div>
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';

export default {
  name: 'Tweet',
  props: {
    user: {
      name: String,
      handle: String,
    },
    timestamp: String,
    message: String,
    image: String,
  },
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions,
  },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
