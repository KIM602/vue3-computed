<template>
    <button @click="add">
        ADD
    </button>
    <h1>{{ reversedMessage }}</h1>
    <h1>{{ reversedMessage }}</h1>
    <h1>{{ reversedMessage }}</h1>
    <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
    data() {
        return {
            //Getter, Setter : 값을 얻어내는 방식과 값을 설정하는 방식으로 사용
            msg: 'Hello Computed!'
        }
    },
    computed: { // 메소드처럼 동작하지만 캐싱기능이 있음
        //Getter : 값을 얻어내는 방식으로만 사용
        // reversedMessage() {
        //     return this.msg.split('').reverse().join('')
        // }

        //Getter, Setter
        reversedMessage: {
            get() {
                return this.msg.split('').reverse().join('')
            },
            set(value) {
                console.log(value)
            }
        }
    },
    methods: {
       add() {
           this.reversedMessage += '!?'
       }
    }
}
</script>