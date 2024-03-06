<template>
    <div class="calculator p-3 mb-4 rounded-3">
        <div class="form-group">
            <label for="num1">Número 1:</label>
            <input type="number" class="form-control" id="num1" v-model="num1" />
        </div>
        <div class="form-group">
            <label for="operation">Operação:</label>
            <select class="form-control" id="operation" v-model="selectedOperation">
                <option value="add">+ (Soma)</option>
                <option value="subtract">- (Subtração)</option>
                <option value="multiply">× (Multiplicação)</option>
                <option value="divide">÷ (Divisão)</option>
            </select>
        </div>
        <div class="form-group">
            <label for="num2">Número 2:</label>
            <input type="number" class="form-control" id="num2" v-model="num2" />
        </div>
        <div class="result">
            <strong>Resultado:</strong> {{ result }}
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            num1: 0,
            num2: 0,
            result: 0,
            selectedOperation: 'add'
        };
    },
    watch: {
        num1() {
            this.calculate();
        },
        num2() {
            this.calculate();
        }
    },
    methods: {
        calculate() {
            switch (this.selectedOperation) {
                case 'add':
                    this.result = this.num1 + this.num2;
                    break;
                case 'subtract':
                    this.result = this.num1 - this.num2;
                    break;
                case 'multiply':
                    this.result = this.num1 * this.num2;
                    break;
                case 'divide':
                    this.result = this.num1 / this.num2;
                    break;
            }
        }
    }
};
</script>

<style scoped>
.calculator {
    max-width: 400px;
    margin: 0 auto;
}

.result {
    margin-top: 10px;
}
</style>