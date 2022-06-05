<template>
  <div class="container">
    <ApprovalsList 
        :ApprovalsList="ApprovalsList"
        :Approve="Approve"
        :Deny="Deny"
    />
  </div>
</template>

<script>
import ApprovalsList from './ApprovalsList';
import { ref } from "@vue/runtime-core";
export default {
  components: {
    ApprovalsList,
  },
  setup() {
    let exampleData = [
      {
        execution_name: 'aaabbb',
        state_machine_name: 'my-first-app',
        task_token: 'aaabbbccc',
        metadata: {},
        actor: '',
        state: 'Pending',
        workflow_expiration: '2022-06-06T12:34:56Z',
        expires_on: '2022-06-13T12:34:56Z',
        last_modified: '2022-06-06T10:34:56Z'
      },
      {
        execution_name: 'aaabbb',
        state_machine_name: 'my-second-app',
        task_token: 'aaabbbccc',
        metadata: {},
        actor: 'Corey',
        state: 'Approved',
        workflow_expiration: '2022-06-06T12:34:56Z',
        expires_on: '2022-06-13T12:34:56Z',
        last_modified: '2022-06-06T10:34:56Z'
      },
      {
        execution_name: 'aaabbb',
        state_machine_name: 'my-first-app',
        task_token: 'aaabbbccc',
        metadata: {},
        actor: 'Corey',
        state: 'Rejected',
        workflow_expiration: '2022-06-06T12:34:56Z',
        expires_on: '2022-06-13T12:34:56Z',
        last_modified: '2022-06-06T10:34:56Z'
      },

    ];
    const Approve = (task_token) => {
      // Do nothing
      console.log(task_token);
    }
    const Deny = (task_token) => {
      // Do nothing
      console.log(task_token);
    }

    return {
      ApprovalsList: ref(exampleData),
      Approve,
      Deny
    };
  }
}
</script>