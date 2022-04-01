<template>
  <v-container>
    <p class="text-h4 text-center indigo lighten-4 py-4">CONTACT</p>
    <p class="text-h5 text-center">SNS</p>
    <div class="text-center">
      <v-btn
      v-for="(account, index) in sns"
      :key="index"
      style="text-transform: none"
      :class="account.color"
      class="ma-4"
      :href="account.url"
      >
        <v-icon>{{account.icon}}</v-icon> {{account.name}} {{account.id}}
      </v-btn>
    </div>
    <div class="text-center mt-4">
      <p class="text-h5">E-Mail</p>
      <p><v-icon>mdi-email</v-icon> kinkitunekin☆gmail.com</p>
      <p>※メールを送る際は、☆を@に変換してください。</p>
    </div>
  </v-container>
</template>

<script>
export default {
  data(){
    return {
      sns:[
        {
          name: 'Twitter',
          id: 'ChanYu1224',
          icon: 'mdi-twitter',
          url: 'https://twitter.com/ChanYu1224',
          color: 'blue lightten-4',
        },
        {
          name: 'Instagram',
          id: 'chan_yu1224',
          icon: 'mdi-instagram',
          url: 'https://www.instagram.com/chan_yu1224/',
          color: 'deep-orange lighten-4'
        },
        {
          name: 'GitHub',
          id: 'ChanYu1224',
          icon: 'mdi-github',
          url: 'https://github.com/ChanYu1224',
          color: 'blue-gray lighten-4',
        }
      ]
    }
  }
}
</script>