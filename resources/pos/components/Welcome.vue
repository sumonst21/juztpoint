<template>
    <v-content>
        <v-container fluid fill-height>
            <v-layout align-center justify-center>
                <v-flex xs12 sm8 md4>
                    <v-card class="elevation-12">
                        <v-toolbar color="primary" dark flat>
                            <v-toolbar-title>Login form</v-toolbar-title>
                            <v-spacer></v-spacer>
                            <v-tooltip bottom>
                                <template v-slot:activator="{ on }">
                                    <v-btn :href="source" icon large target="_blank" v-on="on">
                                        <v-icon>mdi-code-tags</v-icon>
                                    </v-btn>
                                </template>
                                <span>Source</span>
                            </v-tooltip>
                            <v-tooltip right>
                                <template v-slot:activator="{ on }">
                                    <v-btn icon large href="https://codepen.io/johnjleider/pen/pMvGQO" target="_blank" v-on="on">
                                        <v-icon>mdi-codepen</v-icon>
                                    </v-btn>
                                </template>
                                <span>Codepen</span>
                            </v-tooltip>
                        </v-toolbar>
                        <v-card-text>
                            <v-form>
                                <v-text-field label="Login" name="login" prepend-icon="person" type="text"></v-text-field>
                                <v-text-field id="password" label="Password" name="password" prepend-icon="lock" type="password"></v-text-field>
                            </v-form>
                        </v-card-text>
                        <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn color="primary">Login</v-btn>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </v-content>
</template>
<script>
export default {
    props: {
        source: String,
    },
    data: () => ({
        drawer: null,
    }),
}

</script>
