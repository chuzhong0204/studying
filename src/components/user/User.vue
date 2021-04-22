<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>姓名</th>
          <th>性别</th>
          <th>邮箱</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{user.id}}</td>
          <td>{{user.name}}</td>
          <td>{{user.sex}}</td>
          <td>{{user.email}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'user',
  data () {
    return {
      data: '1',
      users: []
    }
  },
  created () {
    this.$axios({
      method: 'get',
      url: '/api/user'
    }).catch(error => {
      console.log('error:' + error)
    }).then(response => {
      this.users = response.data
      // console.log(this.users)
    })
  }
}
</script>

<style scoped>
</style>