<template>
    <!-- html -->
    <h1 @click="increase">{{ count }}</h1>
    <div v-if="count > 4">
        4보다 큽니다!
    </div>
    <ul>
        <Fruit 
        v-for="fruit in fruits"
        :key="fruit"
        :name="fruit">
            {{ fruit }}
        </Fruit>
    </ul>

</template>

<script>
import Fruit from '~/components/Fruit'
// Js(vue)
export default {
    // Fruit 컴포넌트를 갖고 와서 hello라는 이름으로 사용을 함
    components: {
        Fruit
        //Fruit: Fruit 이름이 같으면 value 값은 생략이 가능하다.
    },
    data(){
        return {
            count: 0,
            //반복문을 사용할때 필요한것은 배열데이터
            fruits: ['Apple', 'Banana', 'Cherry']
        }
    },
    methods: {
        increase() {
            // h1 클릭시 숫자가 1씩 증가함
            this.count += 1
        }
    }
}
</script>

<style lang="scss">
    h1 {
        font-size:80px;
        color:violet;
    }
    ul {
        li{
            font-size:40px;
        }
    }
</style>