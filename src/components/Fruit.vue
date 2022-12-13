<template>
    <li>{{ name }}</li>

</template>

<script>
export default {
    props: {
        name: {
            type: String,
            default:''
        }
    }
}
</script>

<style scoped lang="scss"> // scoped로 유효 범위를 설정해서 해당 컴포넌트에서만 style을 관리할 수 있다.
    h1 {
        color:red !important
    }
</style>