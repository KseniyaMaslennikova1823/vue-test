<template>
        <form class="form" @submit.prevent>
                <div style="color: red; font-size: 30px;"> {{ message }} </div>
                <!-- INPUT 1 -->
                <input 
                    class="form__input"  
                    v-for="(elem, index) in getShortList(1)" :key=index 
                    :id="elem.id"
                    :name="elem.name"
                    :text="elem.text"
                    :placeholder="elem.text"
                    value=''  
                    @input="value1 = $event.target.value"                
                >
                <label 
                    class="form__label"
                    v-for="(elem, index) in getShortList(1)" :key=index
                    :for="elem.id"  
                > 
                    {{ elem.name }} : {{ value1 }}
                </label>
                <!-- INPUT 2 -->
                <input 
                    class="form__input"  
                    v-for="(elem, index) in getShortList2(2)" :key=index 
                    :id="elem.id"
                    :name="elem.name"
                    :text="elem.text"
                    :placeholder="elem.text"
                    value=''  
                    @input="value2 = $event.target.value"                
                >
                <label 
                    class="form__label"
                    v-for="(elem, index) in getShortList2(2)" :key=index
                    :for="elem.id"  
                > 
                    {{ elem.name }} : {{ value2 }}
                </label>
                <!-- INPUT 3 -->
                <input 
                    class="form__input"  
                    v-for="(elem, index) in getShortList3(3)" :key=index 
                    :id="elem.id"
                    :name="elem.name"
                    :text="elem.text"
                    :placeholder="elem.text"
                    value=''  
                    @input="value3 = $event.target.value"                
                >
                <label 
                    class="form__label"
                    v-for="(elem, index) in getShortList3(3)" :key=index
                    :for="elem.id"  
                > 
                    {{ elem.name }} : {{ value3 }}
                </label>                
            <button class="form__btn" @click="sendText">Отправить</button>
        </form>
</template>

<script>
export default{
    data() {
        return {
            inputs: [
                {id: 1, name: 'input1', text: 'Введите строку 1'},
                {id: 2, name: 'input2', text: 'Введите строку 2'},
                {id: 3, name: 'input3', text: 'Введите строку 3'},
            ],
            value1:'',
            value2:'',
            value3:'',
            message: '',
            sendValues: { input1: '', input2: '', input3: ''}
        }
    },
    methods: {
        sendText() {
            this.sendValues.input1 = this.value1;
            this.sendValues.input2 = this.value2;
            this.sendValues.input3 = this.value3;

            if ((this.value1 != 0) && (this.value2 !=0) && (this.value3 !=0)) {
                console.log('Your text: ', this.sendValues.input1, this.sendValues.input2, this.sendValues.input3 );
                this.message = '';
            } else {
                this.message = 'Форма пуста';
            }
        },
        getShortList(shortListSize) {
            return this.inputs.slice(0, shortListSize);
        },
        getShortList2(shortListSize) {
            return this.inputs.slice(1, shortListSize);
        },
        getShortList3(shortListSize) {
            return this.inputs.slice(2, shortListSize);
        }
    }
}
</script>

<style lang="scss">
.form {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;

    border: 1px solid purple;
    border-radius: 15px;
    background-color: rgba($color: #AD66D5, $alpha: 0.1);

    width: 70%;
    margin: 50px auto;

    &__input {
            width: 70%;
            height: 50px;

            border: 1px solid purple;
            border-radius: 15px;

            margin-top: 20px;
            margin-bottom: 20px;

            font-size: 25px;
            padding: 0 10px;
    }
    &__label {
        cursor: pointer;
        margin-bottom: 10px;
    }
    &__btn {
        width: 250px;
        height: 50px;
        border: 1px solid purple;
        border-radius: 15px;
        margin-bottom: 20px;
        background-color: #9F3ED5;

        font-size: 32px;

        margin-top: 15px;
    }
}
</style>