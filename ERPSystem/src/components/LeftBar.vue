<template>
  <div class="leftBar">
    <div ref="option">
      <img
        src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/erpnext/img/erpnext-stack-220x234.png"
        alt=""
      />
      <p>基础管理</p>
    </div>
    <div>
      <img
        src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/erpnext/img/erpnext-stack-220x234.png"
        alt=""
      />
      <p>业务管理</p>
    </div>
    <div>
      <img
        src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/erpnext/img/erpnext-stack-220x234.png"
        alt=""
      />
      <p>生产管理</p>
    </div>
    <div>
      <img
        src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/erpnext/img/erpnext-stack-220x234.png"
        alt=""
      />
      <p>采购管理</p>
    </div>
    <div>
      <img
        src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/erpnext/img/erpnext-stack-220x234.png"
        alt=""
      />
      <p>仓库管理</p>
    </div>
    <div>
      <img
        src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/erpnext/img/erpnext-stack-220x234.png"
        alt=""
      />
      <p>财务管理</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {  
       width:0,
       height:0
    };
  },
  mounted () {
    this.observeSize()
  },
  methods: {
    observeSize () {
      const ro = new ResizeObserver(entries => {
        entries.forEach(entry => {
          const { width, height } = entry.contentRect
          this.width = width
          this.height = height
          this.$emit('changed',width)
        })
      })
      ro.observe(this.$refs.option)
    }
  }
}
</script>
<style scoped>
.leftBar {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin: 0 0 0 50px;
}
img {
  max-width: 135px;
  max-height: 135px;
}
p {
  text-align: center;
  margin: 0 0 1em 0;
}
</style>
