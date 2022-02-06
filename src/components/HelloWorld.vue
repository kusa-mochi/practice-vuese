<template>
  <div class="hello">
    <div class="header">
      <!-- ヘッダー -->
      <slot name="header">
        <!-- `<div>デフォルトヘッダー</div>` -->
        <div>デフォルトヘッダー</div>
      </slot>
    </div>
    <h1>{{ msg }}</h1>
    <div class="body">
      <!-- ボディ -->
      <slot>
        <!-- `デフォルトボディ` -->
        デフォルトボディ
      </slot>
    </div>
    <button @click="OnButtonClick">クリックしてね</button>
    <div class="footer">
      <!-- フッター -->
      <slot name="footer">
        <!-- `<div>デフォルトフッター</div>` -->
        <div>デフォルトフッター</div>
      </slot>
    </div>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
  </div>
</template>

<script>
// ふんにゃらほんにゃらコンポーネント
export default {
  methods: {
    /**
     * @vuese
     * 外部仕様としてメソッドの説明が必要な場合にここに説明文を記載する。
     * @arg 引数の説明
     */
    OnButtonClick(e) {
      console.log('クリックされますた。');
      // ボタンがクリックされたときに発火する。
      // @arg パラメータの説明
      this.$emit('onCenterButtonClick', true);
    }
  },
  name: 'HelloWorld',
  props: {
    // ふんにゃらほんにゃらメッセージ
    msg: {
      // `'ほげー'` / `'ふがー'`
      type: String,
      required: false,
      default: 'ほげー'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
