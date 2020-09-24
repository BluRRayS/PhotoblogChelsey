<template>
  <div class="home">
    <!-- Banner -->
    <v-parallax dark src="@/assets/childs.jpeg">
      <v-container align="center" justify="center">
        <v-row>
          <v-col class="text-center mx-auto" cols="4">
            <div>
              <h1 class="display-1 font-weight-thin mb-4">Chelsey Koopman</h1>
              <h4 class="subheading">Photography</h4>
              <v-btn dark icon class="mx-auto" @click="$vuetify.goTo('#Bio')">
                <v-icon size="48px" color="white">mdi-chevron-down</v-icon>
              </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>

    <v-container justify="center" id="Bio">
      <v-row class="pa-12 ">
        <v-col md="2" cols="12">
          <v-img src="@/assets/chelsey.jpeg" aspect-ratio="1" class="grey lighten-2 rounded-circle"></v-img>
        </v-col>
        
        <v-col md="8" cols="12">
          <h1 class="h1 pb-4 ">Fotografie is mijn passie.</h1>
          <p
            class="body-1 "
          >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus voluptas facere, optio debitis deserunt a ipsa architecto vitae non error quibusdam atque, ea quia maiores assumenda ratione aspernatur consequuntur tempore vero dolorum? Nemo quia recusandae delectus harum magni commodi eum suscipit! Obcaecati debitis velit quidem quisquam ipsum sint, expedita ex magnam itaque cumque consequuntur qui officia aliquam illo similique veritatis dolorem recusandae porro veniam facilis quam deleniti suscipit assumenda et. Dolorum accusantium magni, repellat alias, commodi provident illo quo, labore laboriosam natus inventore praesentium magnam doloribus placeat ducimus eligendi ratione amet temporibus esse ipsa. Tenetur, laboriosam rem? Labore, numquam sit?</p>
          <v-btn dark outlined color="teal">Meer over mij</v-btn>
        </v-col>
      </v-row>
    </v-container>

    <v-parallax dark src="@/assets/ivory.jpeg">
      <v-container align="center" justify="center">
        <v-row>
          <v-col class="text-center" cols="12">
            <div>
              <h1 class="display-1 font-weight-thin mb-4">Foto Verhalen</h1>
              <h4 class="subheading">Een blog over fotografie</h4>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>

    <!-- Blog posts -->
    <v-container class="pa-10" id="blogposts">

      <v-row justify="center" align="center">
        <v-col cols="12" md="4" col v-for="post in posts" :key="post.title">
          <v-card shaped raised elevation="5">
            <v-list-item>
              <v-list-item-avatar color="teal">
                <img src="@/assets/chelsey.jpeg" alt="Chelsey" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title class="headline">{{post.title}}</v-list-item-title>
                <v-list-item-subtitle>door Chelsey Koopman</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-img class="white--text align-end" height="250px" src="@/assets/joep.jpeg"></v-img>
            <v-card-subtitle class="pb-0">{{post.subtitle}}</v-card-subtitle>
            <v-card-text class="text--primary">
              <div class="card-text">{{post.desc}}</div>
            </v-card-text>
            <v-card-actions>
              <v-row align="center" class="pr-6 pl-2">
                <v-btn color="teal" text>Lees verder</v-btn>
                <v-spacer />
                <div
                  class="grey--text lighten-2 text-right caption "
                >{{post.date.toLocaleDateString()}}</div>
              </v-row>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<style scoped>
.card-text {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2; /* number of lines to show */
  -webkit-box-orient: vertical;
}
</style>

<script>
export default {
  name: "Home",
  data() {
    return {
      posts: [
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur maxime voluptatem fugit illo! Dolor eveniet natus magni, in inventore repudiandae dolorem culpa, omnis autem reprehenderit voluptatibus ratione maxime velit et eaque cum voluptatum id quis amet? Autem quidem nulla tenetur officiis, porro optio, eos veritatis magni accusantium magnam deleniti at amet mollitia modi eveniet, praesentium fugit ab fuga quisquam nemo? Aliquid, fuga doloribus voluptatibus quidem ullam eligendi? Ab dolores nam cupiditate odio pariatur sapiente veniam, omnis consectetur, sunt eius alias magni tenetur nemo tempora, amet magnam quam in perspiciatis corrupti deleniti placeat. Eveniet facilis sunt, quae assumenda atque earum porro.",
          img: "joep.jpeg",
          date: new Date(),
        },
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur maxime voluptatem fugit illo! Dolor eveniet natus magni, in inventore repudiandae dolorem culpa, omnis autem reprehenderit voluptatibus ratione maxime velit et eaque cum voluptatum id quis amet? Autem quidem nulla tenetur officiis, porro optio, eos veritatis magni accusantium magnam deleniti at amet mollitia modi eveniet, praesentium fugit ab fuga quisquam nemo? Aliquid, fuga doloribus voluptatibus quidem ullam eligendi? Ab dolores nam cupiditate odio pariatur sapiente veniam, omnis consectetur, sunt eius alias magni tenetur nemo tempora, amet magnam quam in perspiciatis corrupti deleniti placeat. Eveniet facilis sunt, quae assumenda atque earum porro.",
          img: "joep.jpeg",
          date: new Date(),
        },
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur maxime voluptatem fugit illo! Dolor eveniet natus magni, in inventore repudiandae dolorem culpa, omnis autem reprehenderit voluptatibus ratione maxime velit et eaque cum voluptatum id quis amet? Autem quidem nulla tenetur officiis, porro optio, eos veritatis magni accusantium magnam deleniti at amet mollitia modi eveniet, praesentium fugit ab fuga quisquam nemo? Aliquid, fuga doloribus voluptatibus quidem ullam eligendi? Ab dolores nam cupiditate odio pariatur sapiente veniam, omnis consectetur, sunt eius alias magni tenetur nemo tempora, amet magnam quam in perspiciatis corrupti deleniti placeat. Eveniet facilis sunt, quae assumenda atque earum porro.",
          img: "joep.jpeg",
          date: new Date(),
        },
        // {
        //   title: "Zwart wit",
        //   subtitle: "Hoe maak in een goed portet",
        //   desc:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur maxime voluptatem fugit illo! Dolor eveniet natus magni, in inventore repudiandae dolorem culpa, omnis autem reprehenderit voluptatibus ratione maxime velit et eaque cum voluptatum id quis amet? Autem quidem nulla tenetur officiis, porro optio, eos veritatis magni accusantium magnam deleniti at amet mollitia modi eveniet, praesentium fugit ab fuga quisquam nemo? Aliquid, fuga doloribus voluptatibus quidem ullam eligendi? Ab dolores nam cupiditate odio pariatur sapiente veniam, omnis consectetur, sunt eius alias magni tenetur nemo tempora, amet magnam quam in perspiciatis corrupti deleniti placeat. Eveniet facilis sunt, quae assumenda atque earum porro.",
        //   img: "joep.jpeg",
        //   date: new Date(),
        // },
      ],
    };
  },
};
</script>
