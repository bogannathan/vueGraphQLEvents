<template src="./index.html"></template>

<script>
export default {
    name: 'AddEventForm',
    props: ['name', 'where', 'when', 'invitees'],
    data() {
        return {
            formInvitees: [],
            addingInvitee: ''
        }
    },
    methods: {
        addInvitee() {
            if (this.addingInvitee.length) {

                this.formInvitees.push(this.addingInvitee)
                this.addingInvitee = ''
                this.$emit('update:invitees', this.formInvitees)
            }
        },
        removeInvitee(index) {
            this.formInvitees.splice(index, 1)
            this.$emit('update:invitees', this.formInvitees)
        }
    },
    computed: {
        syncName: {
            get() { return this.name },
            set(val) { this.$emit('update:name', val) }
        },
        syncWhere: {
            get() { return this.where },
            set(val) { this.$emit('update:where', val) }
        },
        syncWhen: {
            get() { return this.when },
            set(val) { this.$emit('update:when', val) }
        }
    }
}
</script>

<style src='./styles.css' scoped></style>
