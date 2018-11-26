<template src="./index.html"></template>

<script>
export default {
    name: 'Invite',
    props: ['name', 'where', 'when', 'invitees'],
    computed: {
        otherInvitees() {
            let otherInvitees = this.invitees.slice(1); //creates a new copy of array without first entry instead of a new reference

            if (otherInvitees.length == 1) return otherInvitees[0]
            else {
                let lastName = otherInvitees.pop()
                return `${otherInvitees.join(', ')}${otherInvitees.length > 1 ? ',' : ''} and ${lastName}`
            }
        }
    }
}
</script>

<style src='./styles.css' scoped></style>
