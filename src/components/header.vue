<template>
    <v-app-bar app>

      <v-toolbar-title>Random Users</v-toolbar-title>

      <v-spacer></v-spacer>

      <DarkModeSwitch @switched="onSwitched" :initialState="isDarkModeEnabled"/>

    </v-app-bar>
</template>

<script>
    import DarkModeSwitch from 'vue-dark-mode-switch'
    import 'vue-dark-mode-switch/dist/vue-dark-mode-switch.css'
    
    export default {
    name: 'Header',

    data () {
        return {
            isDarkModeEnabled: false,
            }
        },
		components: {
			DarkModeSwitch
		},
		methods: {
			onSwitched: function (isSwitched) {
				console.log('dark mode is enabled :', isSwitched);
			}
		},
}
</script>
