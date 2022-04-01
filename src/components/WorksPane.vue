<template>
  <v-container>
    <p class="text-h4 text-center indigo lighten-4 py-4">WORKS</p>
    <p>Web開発や機械学習等、浅く広く手を伸ばしています。</p>
    <v-slide-group show-arrows>
      <v-slide-item v-for="(work, index) in works" :key="index">
        <v-card width="400px" class="ma-4">
          <v-img
          :src="require(`@/assets/${work.image}`)"
          :aspect-ratio="16/9"
          width="400px"
          ></v-img>
          <v-card-title>
            {{ work.title }}
          </v-card-title>
          <v-card-text>
            <p>最終更新：{{ work.updatedAt }}</p>
            <p>{{ work.description }}</p>
            <v-chip 
            v-for="tag in work.tags"
            :key="tag"
            class="ma-1"
            >{{ tag }}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn
            :href="work.repository"
            class="ml-auto"
            >
              github <v-icon>mdi-github</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-container>
</template>

<script>
  export default {
    data(){
      return {
        works:[
          {
            title: '会員制掲示板',
            image: 'bulletin_board.png',
            tags:[
              'Python3',
              'Django',
              'Django Rest Framework',
              'JavaScript',
              'Vue.js',
              'Vuetify',
            ],
            description: '会員登録を行うことによって、誰とでも掲示板で会話が可能であるサービスです。',
            repository: 'https://github.com/ChanYu1224/bulletin-board-web',
            updatedAt: '2022/03/12',
          },
          {
            title: 'Discordボイスチャンネル通知bot',
            image: 'discord_bot.png',
            tags: [
              'Python3',
              'Discord.py'
            ],
            description: 'チャンネル上で誰かがボイスチャンネルに参加しても、通知が来ないなんて不便ですよね。そんな貴方のために作ったbotです。',
            repository: 'https://github.com/ChanYu1224/discord-voice-channel-alert-bot',
            updatedAt: '2022/02/28',
          },
          {
            title: '強化学習によるおにごっこエージェント',
            image: 'escaper.png',
            tags: [
              'Python3',
              'PyGame',
            ],
            description: 'Pythonを用いて、強化学習を通しておにごっこエージェント（逃げる側）の生成を行いました。アルゴリズムに関してライブラリ等を用いていないので、学習速度が非常に遅い事が難点です。学校の自由課題で作成しました。',
            repository: 'https://github.com/ChanYu1224/escaper-reinforcement-learning',
            updatedAt: '2019/11/29',
          },
          // --template--
          // {
          //   title: '',
          //   image: '',
          //   tags: [],
          //   description: '',
          //   repository: '',
          //   updatedAt: '',
          // }
        ]
      }
    }
  }
</script>
