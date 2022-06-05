<template>
  <table>
      <thead>
          <tr>
              <th>State Machine</th>
              <th>Last Modified</th>
              <th>State</th>
              <th>Actor</th>
              <th>Metadata</th>
              <th>Action</th>
          </tr>
      </thead>
      <tbody>
          <tr v-for="(item, index) in ApprovalsList" :key="index">
            <td>{{item.state_machine_name}}</td>
            <td>{{item.last_modified}}</td>
            <td>{{item.state}}</td>
            <td>{{item.actor}}</td>
            <td>{{item.metadata}}</td>
            <td>
                <div v-if="item.state === 'Pending'">
                    <button @click="Approve(item.task_token)">Approve</button>
                    <span class="delete" @click="Deny(item.task_token)">Deny</span>
                </div>
                <div v-else>&nbsp;</div>             
            </td>
          </tr>
      </tbody>
  </table>
</template>

<script>
export default {
    props: {
        ApprovalsList: Array,
        Approve: Function,
        Deny: Function,
    },
}
</script>