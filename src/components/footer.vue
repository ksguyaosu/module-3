<template>
  <div class="footer">
    <img src="../assets/logo.png" />
    <h1>Подпишитесь на новости</h1>
    <p>
      Оставьте свой email и вы будите получать актуальную информацию о наших
      акциях и новинках
    </p>
    <div class="form">
      <input type="text" name="name" id="name" placeholder="Введите email" />
      <button>Подписаться</button>
    </div>
  </div>
</template>

<script>
export default {
  name: `footers`,
};
</script>

<style scoped>
img {
  margin-top: 49px;
  width: 167px;
  height: 40px;
  margin-bottom: 43px;
}
h1 {
  margin-bottom: 7px;
}
p {
  width: 406px;
  margin: auto;
}
input[type="text"] {
  border: 0.5px solid black;
  width: 275px;
  height: 37px;
  padding: 5px;
  border-radius: 4px;
  margin-right: 10px;
  margin-top: 15px;
  margin-bottom: 80px;
}
button {
  border: 0.5px solid black;
  width: 127px;
  height: 47px;
  font-size: 15px;
  margin-top: 15px;
  margin-bottom: 80px;
  background: #d9d9d9;
}
.footer {
  margin-top: 95px;
  background-color: #d9d9d9;
}
</style>
