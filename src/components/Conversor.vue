<template>
  <div class="principal">
    <h1>Bin<span class="num2">2</span>Dec Converter</h1>
    <p class="paragraph">Convert Binary to Decimal or Decimal to Binary</p>
    <p v-if="decimal" class="label">From Decimal to Binary</p>
    <p v-else class="label">From Binary to Decimal</p>
    <div class="divSeparator">
      <div>
        
        <input
          class="inputs"
          type="number"
          v-model="valor"
          placeholder="Type the value"
        />
      </div>
      <div class="btn-con">
        <button @click="fazConversao" className="button">Convert</button>
        <button @click="inverteOperacao" className="button">Reverter</button>
      </div>

      <div class="res">
        <p class="result">{{ valor_res }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Conversor",
  data() {
    return {
      decimal: true,
      valor: "",
      valor_res: "",
    };
  },
  methods: {
    inverteOperacao() {
      this.decimal = !this.decimal;
      this.valor_res = "";
      this.valor = "";
    },
    fazConversao() {
      if (this.decimal == true) {
        let num = this.valor;
        let bin = (num % 2).toString();
        for (; num > 1; ) {
          num = parseInt(num / 2);
          bin = (num % 2) + bin;
        }
        this.valor_res = bin;
      } else {
        let bin = this.valor.toString()
        let dec = 0;
        for (let c = 0; c < bin.length; c++)
          dec += Math.pow(2, c) * bin[bin.length - c - 1];
          this.valor_res = dec;
      }
    },
  },
};
</script>

<style scoped>
h1,
p {
  text-align: center;
}
.divSeparator {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  padding: 0;
  text-align: left;
}
.inputs {
  display: flex;
  margin: 0 auto;
  box-sizing: border-box;
  padding: 15px;
  border-radius: 15px;
  border: none;
  width: 22em;
}
::-webkit-input-placeholder {
  color: #060808;
  font-size: 12px;
}
.principal {
  padding: 8px;
  border: none;
  width: 25%;
  height: 450px;
  margin: 0 auto;
  background: #f2f2f2;
  border-radius: 15px;
  -webkit-box-shadow: 1px 4px 23px 3px rgba(0, 0, 0, 0.52);
  box-shadow: 1px 4px 23px 3px rgba(0, 0, 0, 0.52);
  font-family: "Plus Jakarta Sans", sans-serif;
}
.label {
  padding-top: 1px;
  text-align: center;
  font-size: 1.5em;
  color: #418d83;
  font-family: "Plus Jakarta Sans", sans-serif;
}
.label:after {
  padding-right: 5px;
}
.button {
  border: none;
  padding: 20px;
  cursor: pointer;
  background: #418d83;
  color: #fff;
  border-radius: 25px;
  margin-top: 10px;
  transition: linear 0.5s;
  font-size: 15px;
  width: 8em;
  font-size: 1em;
}
.button:hover {
  background: #2eccb7;
}
.num2 {
  color: #418d83;
}
.paragraph {
  color: #8a8a8a;
  font-size: 12px;
}
.btn-con{
  display: flex;
  gap: 2em;
}
.result{
  font-size: 2em;
}
</style>
