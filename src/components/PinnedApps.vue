<template>
  <div>
    <v-row>
      <v-col cols="12" sm="6" md="4" v-for="app in apps" :key="app.id">
        <v-hover v-slot:default="{ hover }">
          <v-card
            :href="app.playstoreUrl"
            target="_blank"
            :elevation="hover ? 12 : 2"
            class="rounded-lg"
          >
            <v-card-title>{{ app.title }}</v-card-title>
            <v-card-text>{{ app.summary }}</v-card-text>
            <v-img :src="app.icon" max-height="150" contain></v-img>
            <v-card-title class="mb-2">
              <v-icon left class="mr-1">mdi-star-outline</v-icon>
              {{ app.scoreText }}
            </v-card-title>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "PinnedApps",
  data: () => ({
    apps: [
      {
        title: "Share Karo",
        appId: "com.japangor.sharekaro",
        url: "http://localhost:3000/api/apps/com.japangor.sharekaro",
        icon:
          "https://lh3.googleusercontent.com/C8fGmPEhY3DSte952ETgzGfXZRB66rk9tKIYz-Fkie8zy-Cxvjdj5Lf_bNw38hyvdt8=s180-rw",
    
        developerId: "FieldAssist",
        priceText: "FREE",
        price: 0,
        free: true,
        summary: "SHARE-Karo is alternative of share it file transfer with excellent sharing and fast transfer speed & without useless ads and also has text sharer feature to share your writings with anyone via barcode",
        scoreText: "4.2",
        score: 3.88,
        playstoreUrl:
          "https://play.google.com/store/apps/details?id=com.japangor.gjamshare",
       
      },   {
        title: "Learn to code HTML",
        appId: "com.japangor.note",
        url: "https://play.google.com/store/apps/details?id=com.japangor.learntocodeo",
        icon:
          "https://lh3.googleusercontent.com/VRrb_RmBPIYJF0TC3NwW_EvErEadhzG-Ru_NlybfPp_XacRSLAD43txl1iKh-eJw0Mk=s180-rw",
    
        developerId: "FieldAssist",
        priceText: "FREE",
        price: 0,
        free: true,
        summary: "This FREE app will teach you how to design a web page using HTML.In our interactive HTML courseware Learn To Code (HTML) will help you to Learn Html",
        scoreText: "3.9",
        score: 3.88,
        playstoreUrl:
          "https://play.google.com/store/apps/details?id=com.japangor.learntocode",
       
      },
          {
        title: "GJAM NOTES",
        appId: "com.japangor.note",
        url: "http://localhost:3000/api/apps/com.japangor.sharekaro",
        icon:
          "https://lh3.googleusercontent.com/UfNNiBCoZeWH4vjr7rosZqJ3scu1Cb5fEvmcPEXf3YV5E4JlIr2mputu8pu8fb8CneM=s180-rw",
    
        developerId: "FieldAssist",
        priceText: "FREE",
        price: 0,
        free: true,
        summary: "GJAM Notes is a simple and awesome notepad app. It gives you a quick and simple notepad editing experience when you write notes, memos, e-mails, messages, shopping lists and to-do lists. Taking notes with GJAM is easier than any other notepad or memo pad app.",
        scoreText: "4.8",
        score: 3.88,
        playstoreUrl:
          "https://play.google.com/store/apps/details?id=com.japangor.note",
       
      },
    ]
  })
};
</script>

<style></style>
