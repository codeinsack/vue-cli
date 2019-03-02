<template>
  <div class="component">
    <h1>The User Component</h1>
    <p>I'm an awesome User!</p>
    <button @click="changeName">
      Change my Name
    </button>
    <p>Name is {{ name }}</p>
    <p>Age is {{ age }}</p>
    <hr>
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <app-user-detail
          :my-name="name"
          :reset-fn="resetName"
          :user-age="age"
          @nameWasReset="name = $event"
        />
      </div>
      <div class="col-xs-12 col-sm-6">
        <app-user-edit
          :user-age="age"
          @ageWasEdited="age = $event"
        />
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from './UserDetail.vue';
import UserEdit from './UserEdit.vue';

export default {
  components: {
    appUserDetail: UserDetail,
    appUserEdit: UserEdit,
  },
  data() {
    return {
      name: 'Max',
      age: 27,
    };
  },
  methods: {
    changeName() {
      this.name = 'Anna';
    },
    resetName() {
      this.name = 'Max';
    },
  },
};
</script>

<style scoped>
  div {
    background-color: lightblue;
  }
</style>
