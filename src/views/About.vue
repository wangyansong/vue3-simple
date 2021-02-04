<template>
  <div>
    <a-date-picker @change="onChange" />
    <a-form :model="form" :label-col="labelCol" :wrapper-col="wrapperCol">
      <a-form-item label="Activity name">
        <a-input v-model:value="form.name" />
      </a-form-item>
      <a-form-item label="Activity zone">
        <a-select v-model:value="form.region" placeholder="please select your zone">
          <a-select-option value="shanghai">
            Zone one
          </a-select-option>
          <a-select-option value="beijing">
            Zone two
          </a-select-option>
        </a-select>
      </a-form-item>
    </a-form>
  </div>
</template>
<script>
export default {
  name: 'About',
  data () {
    return {
      userName: null,
      form: {
        name: null,
        region: null
      },
      labelCol: { span: 4 },
      wrapperCol: { span: 14 }
    }
  },
  mounted () {
  },
  methods: {
    onChange (date, dateString) {
      console.log(date, dateString)
    }
  }
}
</script>
