<template>
  <div>
    <table>
      <tr>
        <td>医生编号</td>
        <td>医生姓名</td>
        <td>医生科室</td>
        <td>医生年龄</td>
        <td>医生学历</td>
        <td>医生是否上班</td>
      </tr>
      <tr v-for="item in doctors">
        <td>{{item.num}}</td>
        <td>{{item.name}}</td>
        <td>{{item.office}}</td>
        <td>{{item.age}}</td>
        <td>
          <span v-if="item.edu==1">专科</span>
          <span v-if="item.edu==2">本科</span>
          <span v-if="item.edu==3">硕士</span>
          <span v-if="item.edu==4">博士</span>
          <span v-if="item.edu==5">博士后</span>
        </td>
        <td>
          <span v-if="item.status==1">是</span>
          <span v-if="item.status==0">否</span>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'Doctors',
    data() {
      return {
        msg: '',
        doctors: [
          {
            num: 20170706225213,
            name: '扁鹊',
            office: '心内科',
            age: 25,
            edu: 5,
            status: 1
          },
          {
            num: 20170706225213,
            name: '扁鹊',
            office: '心内科',
            age: 25,
            edu: 2,
            status: 1
          },
          {
            num: 20170706225213,
            name: '扁鹊',
            office: '心内科',
            age: 25,
            edu: 4,
            status: 0
          }
        ]
      }
    },
    created () {

    }
  }
</script>

<style scoped>

</style>
