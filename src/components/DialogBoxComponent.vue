<script lang="ts">
import {defineComponent, ref} from 'vue'
import {Microphone, Paperclip} from "@element-plus/icons-vue";


/**
 * 下方的对话框组件,需要支持对话、文件和图片等多种形式
 */
export default defineComponent({
  name: "DialogBoxComponent",
  components: {Paperclip, Microphone},
  setup() {
    const query = ref("");
    return {
      query
    }
  }
})
</script>

<template>
  <div class="wrapper">
    <div class="dialogBox">
      <textarea class="inputArea" placeholder="发消息、输入 @ 或 / 选择技能"/>
      <div class="tool">
        你好
        <el-icon>
          <Paperclip/>
        </el-icon>
        <el-icon size="14px">
          <Picture/>
        </el-icon>
        <el-icon size="14px">
          <Microphone/>
        </el-icon>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: block;
}

.dialogBox {
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
}

.tool {
  display: flex;
}
</style>