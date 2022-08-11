<template>
  <div className="tweet">
    <ImageComp :image="image" />
    <div className="body">
      <div className="top">
        <UserComp :user="user" />
        <!-- <span className="user">
          <span className="name">Name</span>
          <span className="handle">handle</span>
        </span> -->
        <TimeStamp :timestamp="timestamp" />
      </div>
      <MessageComp :message="message" />
      <ActionsComp />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>
<script>
import MessageComp from "./MessageComp.vue";
import UserComp from "./UserComp.vue";
import TimeStamp from "./TimeStamp.vue";
import ImageComp from "./ImageComp.vue";
import ActionsComp from "./ActionsComp.vue";
export default {
  components: { TimeStamp, UserComp, MessageComp, ImageComp, ActionsComp },
  name: "Tweet",

  props: {
    user: Object,
    timestamp: String,
    message: String,
    image: String,
  },

  data() {
    return {};
  },
  methods: {},
  computed: {},
  watch: {},
};
</script>
<style scoped>
a {
  color: #42b983;
}
</style>
