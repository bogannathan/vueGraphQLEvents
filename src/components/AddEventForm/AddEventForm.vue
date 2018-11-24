<template src="./index.html"></template>

<script>
export default {
    name: 'AddEventForm',
    props: ['name', 'where', 'when', 'invitees'],
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
        },
        syncWho: {
            get() { return this.invitees },
            set(val) { this.$emit('update:invitees', val) }
            //figure out cool way
        }
    }
}
</script>

<style src='./styles.css' scoped></style>
