<template>
  <v-dialog max-width="600px">
    <template v-slot:activator="{ on, attrs }">
      <v-btn color="success" v-bind="attrs" v-on="on">
        Add new project
      </v-btn>
    </template>
    <v-card>
      <v-card-title>
        <h2>Add a New Project</h2>
      </v-card-title>
      <v-card-text>
        <v-form class="px-3" ref="form">
          <v-text-field
            label="Title"
            v-model="title"
            prepend-icon="mdi-folder"
            :rules="inputRules"
          ></v-text-field>
          <v-textarea
            label="Information"
            v-model="content"
            prepend-icon="mdi-pencil-outline"
            :rules="inputRules"
          ></v-textarea>

          <v-menu
            v-model="menu"
            :close-on-content-click="false"
            max-width="290"
          >
            <template v-slot:activator="{ on, attrs }">
              <v-text-field
                :value="computedDateFormattedMomentjs"
                prepend-icon="mdi-calendar"
                clearable
                label="Due date"
                readonly
                v-bind="attrs"
                v-on="on"
                @click:clear="date = null"
                :rules="inputRules"
              ></v-text-field>
            </template>
            <v-date-picker
              v-model="date"
              @change="menu = false"
            ></v-date-picker>
          </v-menu>

          <v-spacer></v-spacer>
          <v-btn text class="success mx-0 mt-3" @click="submit"
            >Add Project</v-btn
          >
        </v-form>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
import moment from 'moment'

export default {
  name: 'Popup',
  data() {
    return {
      title: '',
      content: '',
      date: null,
      menu: false,
      inputRules: [
        v => v.length>=3 || 'Minimum length is 3 characters'
      ]
    }
  },
  methods: {
    submit() {
      if(this.$refs.form.validate()) {
        console.log(this.title, this.content)
      }
    },
  },

  computed: {
    computedDateFormattedMomentjs() {
      return this.date ? moment(this.date).format('Do MMM YYYY') : ''
    },
  },
}
</script>
