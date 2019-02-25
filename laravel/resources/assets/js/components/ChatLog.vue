<template>
    <div>
        <div>在线人数: <span>{{ online_number.length }}</span></div>
        <div v-for="(message, index) in messages" 
            class="chat-log" :key="index">
            <chat-message :message="message"></chat-message>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['messages', 'online_number'],
    }
</script>

<style scoped>
    .chat-log:nth-child(even) {
        background-color: #77777730;
    }
</style>