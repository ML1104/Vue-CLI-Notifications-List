<template>
    <div>
        <div class="notification" v-for="notification in notifications" v-bind:key="notification[0]">
            <div class="timestamp">{{ notification.timestamp }}</div>
            <div class="message">{{ notification.message }}</div>
            <div class="wrapper"><img class="icon" :src="notification.icon"></div>
            <div class="seen">{{ notification.seen }}</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Notifications',


  data() {
    return {
      notifications: [],
    }
  },

  mounted() {
    this.axios.get('http://api.myjson.com/bins/19wyhe')
        .then((response) => {
            // eslint-disable-next-line
            console.log(response.data);
            // couldn't get sorting to work
            // this.notifications.sort((arrayItemOne, arrayItemTwo) => {
            //     return arrayItemOne - arrayItemTwo;
            // })
            this.notifications = response.data;
        })
  },

}
</script>

<style scoped>

.notification {
    border: 1px solid black;
    margin-left: 25%;
    width: 50%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100px;
}

.timestamp {
    border-right: 1px solid black;
    width: 25%;
    padding-top: 40px;
    padding-bottom: 40px;
}

.message {
    border-right: 1px solid black;
    background-color: wheat;
    width: 25%;
    padding-top: 32px;
    padding-bottom: 32px;
}

.icon {
    width: 50px;
    height: 50px;
    padding-top: 27px;
    padding-bottom: 27px;
}

.seen {
    width: 25%;
    padding-top: 40px;
    padding-bottom: 40px;
}

.wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 25%;
    border-right: 1px solid black;
}

.grey {
    background-color: rgba(166, 169, 173, 0.5);
}

</style>
