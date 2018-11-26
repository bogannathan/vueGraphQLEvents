<template>
<div class="content container">
    <div>
        <AddEventForm :name.sync="name" :where.sync="where" :when.sync="when" :invitees.sync="invitees"/>
    </div>
    <div>
        <Invite :name="name" :where="where" :when="when" :invitees="invitees" />
    </div>
</div>
</template>

<script>
import AddEventForm from '@/components/AddEventForm/AddEventForm.vue'
import Invite from '@/components/Invite/Invite.vue'


export default {
    name: 'AddEvent',
    components: {
        AddEventForm,
        Invite
    },
    methods: {
        printit() {
            /* eslint-disable */
            console.log('this', this.name, this.where, this.when, this.invitees)
        }
    },
    data() {
        return {
            name: '',
            where: '',
            when: '',
            invitees: []
        }
    }
}
</script>

<style scoped>
.content {
  display: flex;
}

.content div {
  flex: 1;
}
</style>
