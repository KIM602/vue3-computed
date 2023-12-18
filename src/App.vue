<template>
    <h1>{{ reversedMessage }}</h1>
    <h1>{{ reversedMessage }}</h1>
    <h1>{{ reversedMessage }}</h1>
    <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
    data() {
        return {
            msg: 'Hello Computed!'
        }
    },
    computed: { // 메소드처럼 동작하지만 캐싱기능이 있음
        reversedMessage() {
            return this.msg.split('').reverse().join('')
        }
    }
}
</script>