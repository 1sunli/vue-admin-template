<template>
  <div>
    <el-upload
      ref="upload"
      drag
      action="/files/"
      :auto-upload="false"
      :on-success="onSuccess"
    >
      <i class="el-icon-upload" />
      <div class="el-upload__text">将文件拖到此处，或<em>点击上传</em></div>
    </el-upload>
    <el-button style="margin-left: 10px;" size="small" type="success" @click="submitUpload">上传到服务器</el-button>
  </div>
</template>

<script>

export default {
  name: 'UploadDemo',
  methods: {
    submitUpload() {
      this.$refs.upload.submit()
    },
    onSuccess() {
      this.$message.success('上传成功')
    }
  }
}
</script>
