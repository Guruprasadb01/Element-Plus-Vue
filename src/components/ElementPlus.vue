<template>
  <div class="demo-wrapper">
    <h1>Element Plus Demo</h1>

    <el-button type="primary">Primary Button</el-button>

    <el-input v-model="text" placeholder="Type here" class="mt" />

    <el-select v-model="selected" placeholder="Select item" class="mt">
      <el-option label="Option 1" value="1" />
      <el-option label="Option 2" value="2" />
    </el-select>

    <el-date-picker v-model="date" type="date" placeholder="Pick a date" class="mt" />

    <el-switch v-model="switchValue" class="mt" />

    <el-checkbox-group v-model="checkedList" class="mt">
      <el-checkbox label="Option A" />
      <el-checkbox label="Option B" />
    </el-checkbox-group>

    <el-radio-group v-model="radio" class="mt">
      <el-radio label="One" />
      <el-radio label="Two" />
    </el-radio-group>

    <el-slider v-model="slider" class="mt" />

    <el-rate v-model="rating" class="mt" />

    <el-progress :percentage="50" class="mt" />

    <el-alert title="Info Alert" type="info" class="mt" />

    <el-dialog v-model="dialogVisible" title="Hello">
      <span>This is a dialog</span>
    </el-dialog>

    <el-button @click="dialogVisible = true" class="mt">Open Dialog</el-button>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const text = ref('')
const selected = ref('')
const date = ref('')
const switchValue = ref(false)
const checkedList = ref<string[]>([])
const radio = ref('')
const slider = ref(30)
const rating = ref(3)
const dialogVisible = ref(false)
</script>

<style scoped>
.demo-wrapper {
  max-width: 600px;
  margin: auto;
  padding: 24px;
  display: flex;
  flex-direction: column;
}
.mt {
  margin-top: 20px;
}
</style>