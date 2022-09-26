<template>
  <div class='tweet'>
    <img :src="image" class="profile" alt="profile"/>
    <div class='body'>
      <div class='top'>
        <span class='user'>
          <span class="name">{{ name }}</span>
          <span class="handle">{{ handle }}</span>
        </span>
        <span class="timestamp">{{ timestamp }}</span>
      </div>
      <p class="message">{{ message }}</p>
      <div class="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
export default {
  name: 'Tweet',
  data: () => ({
    tweets: [
      {
        id: 1,
        user: {
          name: 'Thoughts of Dog®',
          image: 'https://i.imgur.com/b0EdHVV.jpg',
          handle: 'dog_feelings',
        },
        timestamp: '1h ago',
        message: 'the human likes to say. that i live here rent free. but i would argue. this housing accommodation. is my payment. for a lifetime of love. and excellent company',
      },
      {
        id: 2,
        user: {
          name: 'Thoughts of Dog®',
          image: 'https://i.imgur.com/b0EdHVV.jpg',
          handle: 'dog_feelings',
        },
        timestamp: '2h ago',
        message: 'sometimes. the human presses their noggin against mine. to figure out what i’m thinking. so i just think really hard. about how much i love them. and hope they figure it out',
      },
      {
        id: 3,
        user: {
          name: 'Thoughts of Dog®',
          image: 'https://i.imgur.com/b0EdHVV.jpg',
          handle: 'dog_feelings',
        },
        timestamp: '3h ago',
        message: 'here is what. i plan to accomplish today: \n\n2. bark loudly. but at nothing \n7. lose my ball under the couch\n7b. politely ask the human. to get my ball\n3. immediately lose it again. under the same couch\n4. big nap. you have worked hard\n2. repeat',
      },
    ],
  }),
  props: {
    name: {
      type: String,
    },
    image: {
      type: String,
    },
    handle: {
      type: String,
    },
    timestamp: {
      type: String,
    },
    message: {
      type: String,
    },
  },
};
</script>

<style scoped>
.tweet {
    margin: 0 auto;
    min-width: 480px;
    max-width: 640px;
    min-height: 80px;
    padding: 10px;
    border: 1px solid #ccc;
    display: flex;
    font-size: 1.1rem;
    line-height: 18px;
  }

  .body {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

 a {
  color: #42b983;
}

  .top {
    display: flex;
    line-height: 1.4rem;
  }

  .more {
    margin-left: 20px;
  }

  .profile {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    margin-right: 10px;
  }

  .name {
    font-weight: bold;
    margin-bottom: 0.5em;
    margin-right: 0.3em;
  }

  .handle {
    color: #536471;
    margin-left: 3px;
    margin-right: 3px;
  }

  .timestamp {
    color: #536471;
    font-size: 1.1rem;
  }

  .timestamp::before {
    content: "·";
    padding-right: 0.3em;
    font-size: 1.1rem;
    font-weight: 600;
  }

  .message {
    text-align: left;
    font-stretch: 100%;
    font-weight: 400;
    line-height: 1.6rem;
    overflow-wrap: break-word;
    white-space: pre-wrap;
  }

  .actions {
    padding: 5px 5px;
    width: 360px;
    display: flex;
    justify-content: space-between;
    color: #536471;
  }
</style>
