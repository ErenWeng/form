<template>
  <v-container fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md4>

        <v-form>
          <v-card class="elevation-12">
            <v-toolbar dark color="cyan darken-1">
              <v-toolbar-title>
                Login form
              </v-toolbar-title>
            </v-toolbar>
            <v-card-text>
              <v-text-field
                prepend-icon="email"
                name="email"
                label="Email"
                type="text"
              >
              </v-text-field>

              <v-text-field
                prepend-icon="lock"
                name="password"
                label="Password"
                type="password"
              >
              </v-text-field>
            </v-card-text>

            <v-divider light>
            </v-divider>

            <v-flex align-center justify-between>
              <v-card-actions>
                  <v-btn>Sign up</v-btn>
                  <v-spacer></v-spacer>
                  <v-btn dark color="cyan darken-1">Login
                    <v-icon>keyboard_arrow_right</v-icon>
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
    name: "login"
  };
</script>

<style lang="scss" scoped>

</style>
