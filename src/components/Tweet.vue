<template>
  <div className="tweet">
    <ProfileImg :image="user.image"/>

    <div className="body">
      <div className="top">
        <User :user="user"/>
        <Timestamp :timestamp="timestamp"/>
      </div>

      <Message :message="message"/>

      <Actions :actions="actions"/>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImg from './ProfileImg.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';
export default {
  props: {
    user: {
      name: String,
      image: String,
      handle: String,
    },
    timestamp: String,
    message: String,
  },
  components: {
    ProfileImg,
    User,
    Timestamp,
    Message,
    Actions,
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
