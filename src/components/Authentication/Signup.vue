<template>
  <v-container fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md4>

        <v-form>
          <v-card class="elevation-12">
            <v-toolbar dark color="indigo darken-1">
              <v-toolbar-title>
                Signup form
              </v-toolbar-title>
            </v-toolbar>

            <v-card-text>
              <v-alert
                :value="true"
                color="error"
                dense
                outlined
                icon="warning"
              >
                This user already exist, try a different set of data.
              </v-alert>

              <v-text-field
                prepend-icon="person"
                name="user name"
                label="User name"
                type="text"
                :rules="[rules.required]"
              >
              </v-text-field>

              <v-text-field
                prepend-icon="email"
                name="email"
                label="Email"
                type="text"
                :rules="[rules.required, rules.email]"
              >
              </v-text-field>

              <v-text-field
                prepend-icon="lock"
                name="password"
                label="Password"
                type="password"
                :rules="[rules.required]"
                v-model="password"
              >
              </v-text-field>

              <v-text-field
                prepend-icon="enhanced_encryption"
                name="Confirm password"
                label="confirm password"
                type="password"
                :rules="[rules.required]"
                :error="valid()"
                v-model="confirm_password"
              >
              </v-text-field>
            </v-card-text>

            <v-divider light>
            </v-divider>

            <v-flex align-center justify-between>
              <v-card-actions>
                <v-btn>Login</v-btn>
                <v-spacer></v-spacer>
                <v-btn dark color="indigo darken-1">Registerd
                  <v-icon>keyboard_arrow_up</v-icon>
                </v-btn>
              </v-card-actions>
            </v-flex>
          </v-card>
        </v-form>

      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      password: '',
      confirm_password: '',
      rules: {
        required: value => !!value || "Required.",
        email: value => {
          const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
          return pattern.test(value) || "Invalid e-mail.";
        }
      }
    }),
    methods: {
      valid() {
        return this.password !== this.confirm_password
      }
    }
  };
</script>

<style lang="scss" scoped>

</style>
