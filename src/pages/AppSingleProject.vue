<script>
import ProjectsListCard from "../components/ProjectsListCard.vue";
import AppLoader from "../components/AppLoader.vue";
import axios from "axios";

export default {
  data() {
    return {
      singleProject: null,
      apiUrl: "http://127.0.0.1:8000/api/projects",
    };
  },
  name: "AppSingleProject",
  components: { ProjectsListCard, AppLoader },
  methods: {
    getSingleProject() {
      console.log("ID passato:", this.$route.params.id);
      axios
        .get(`${this.apiUrl}/${this.$route.params.id}`)
        .then((response) => {
          console.log(response.data.results);
          this.singleProject = response.data.results;
          this.loaded = true;
        })
        .catch(function (error) {
          console.log(error);
        });
    },
  },

  created() {
    this.getSingleProject();
  },
  computed: {
    loaded() {
      return this.singleProject !== null;
    },
  },
};
</script>

<template>
  <!--<ProjectsListCard />-->
  <h2>Single Project Page ID:{{ $route.params.id }}</h2>

  <p>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Saepe, ipsam vero.
    Facilis quos facere consectetur velit, natus vitae pariatur perspiciatis,
    ipsum alias repudiandae incidunt fugit laborum, aperiam reprehenderit
    accusantium nemo! Amet hic, modi at explicabo dolore neque commodi,
    voluptatibus error maiores officia ut incidunt a pariatur voluptas ratione
    sint similique unde perferendis non, nobis optio maxime cupiditate ullam
    corrupti? Autem. Delectus, quae porro nesciunt sequi vero suscipit
    distinctio modi adipisci repudiandae numquam error maxime maiores dolorem
    repellat a laudantium repellendus ipsum cumque fugit odit eligendi magni
    explicabo illo! Quia, maxime? Omnis accusamus voluptatibus aut quasi
    officiis! Quasi aperiam porro mollitia quaerat obcaecati distinctio nulla
    repudiandae, cum debitis, animi quia enim tempora molestiae praesentium
    perferendis beatae consectetur provident corrupti eius architecto? Culpa ex,
    blanditiis modi corporis quaerat, assumenda harum magnam est cumque, nihil
    reiciendis repellendus nesciunt. Temporibus nostrum voluptate tempore,
    officia, quam, blanditiis vero praesentium suscipit nulla amet expedita
    minima eius. Facere laboriosam asperiores non reiciendis, explicabo aperiam
    culpa ex hic repellendus sunt doloribus natus a eius dolorum esse
    dignissimos animi ratione mollitia minus voluptates soluta minima rerum.
    Tempora, sequi quidem. Error ipsam accusamus facilis laboriosam eaque,
    repellat eveniet soluta iusto atque hic labore quo modi mollitia a nostrum
    vitae sapiente in voluptatem fugiat nihil. Assumenda illo quasi in eaque
    eum. Harum soluta optio dignissimos corporis alias sit quis autem! Dicta
    saepe, fuga nam tempora ducimus vel totam perspiciatis quam suscipit soluta
    maiores ex quidem recusandae ea omnis, quis praesentium repellat. Sapiente
    alias mollitia enim est odio, ea, impedit nam nihil quas sunt omnis,
    suscipit perferendis consectetur? Quia perferendis, consequuntur, quo
    quisquam quis, dolores pariatur laudantium minus dolorem sequi adipisci
    aperiam? Sunt eveniet blanditiis consequuntur fugiat libero maiores enim
    saepe, omnis voluptas? A deleniti illo porro corrupti repellendus qui aut
    reprehenderit maxime, placeat laboriosam voluptatum fugiat iure veritatis
    autem obcaecati similique. Recusandae sit aperiam cumque ad repudiandae eius
    sequi. Nemo quod, autem enim asperiores non iste odio atque beatae quaerat
    optio a quibusdam veniam architecto odit nulla porro dolores reprehenderit
    libero! Sunt, maiores laborum possimus consequatur incidunt velit. Sequi,
    dicta eius blanditiis, asperiores maxime hic natus facilis deserunt
    repudiandae ad quia et odit autem iste animi aut earum at quod nulla?
    Dolorem modi a tenetur nam possimus illo fugiat est iusto magnam voluptatem,
    commodi ex, et facere perferendis quo veniam, esse eligendi quas officia
    beatae necessitatibus! Ab sapiente quis natus iure? Asperiores consequuntur
    temporibus at laborum architecto, quia doloremque tenetur ipsam obcaecati
    voluptates vero cumque quis maxime adipisci nisi provident minima sed
    necessitatibus expedita consequatur repellat. Incidunt repellat delectus
    dolore ipsum! Quo a veniam delectus id possimus ipsam commodi voluptates
    repudiandae! Omnis debitis iure cum dicta ab corrupti officia consectetur
    aliquam incidunt tenetur modi nemo, quibusdam voluptate provident,
    dignissimos error illum? Ab consequuntur fugiat repudiandae quam voluptates
    veritatis ad laudantium corporis, nostrum possimus nam, sed repellendus
    minima alias. At repudiandae quasi minima? Modi esse ipsum enim in earum
    dignissimos odio aliquam! In totam perspiciatis qui eos quo nemo ut eligendi
    dolor impedit tempora maxime vero cupiditate ad, laborum repellat maiores
    porro nulla ipsum modi, asperiores sapiente a eum autem. Quo, officia!
    Molestiae, officia nam repellat quam cumque quibusdam necessitatibus sed
    minus minima nihil velit autem qui distinctio reiciendis veniam dolore
    laborum sit magnam neque error ea repudiandae! Commodi velit suscipit
    eveniet! Atque rerum iusto eligendi praesentium consequuntur eum veniam
    dolor in consequatur nobis. Doloribus sit expedita error assumenda saepe.
    Est, quis officia dolorem expedita neque debitis cum doloremque nobis a?
    Ipsa? Maxime omnis hic dolorum distinctio animi porro cumque aperiam quia
    ipsa modi sint neque quaerat ab, similique suscipit exercitationem
    doloremque debitis, recusandae eos cupiditate qui nihil quae quis veritatis.
    Alias! Voluptatem nesciunt repellendus, aliquid amet at aut dolorem ipsum,
    voluptates eos veniam nihil officiis impedit exercitationem reiciendis! Iure
    vitae iste sequi ducimus, sed provident molestiae at exercitationem optio
    accusantium vero! Quisquam commodi atque temporibus adipisci expedita
    veritatis magnam reiciendis ab molestias modi animi nihil aliquid incidunt
    dicta consectetur, eum enim mollitia non, laborum natus cumque illo, quas
    omnis! Dolorum, dolorem. Expedita atque velit neque perspiciatis quae
    deleniti nisi esse, nihil dolor porro soluta, voluptates voluptatibus!
    Suscipit impedit quo autem non, deleniti atque sequi illo ullam laudantium
    quaerat illum possimus quibusdam! Suscipit nemo aut possimus minus fugiat
    vel expedita laboriosam est ipsum. Rem quasi nobis dolore nesciunt
    cupiditate officiis esse doloribus dolorum ratione fuga? Quidem iure,
    placeat repellat cum ut maiores. Aliquam tempore quisquam molestiae
    accusamus iste harum architecto, autem magni laboriosam, placeat dolores
    consequatur eligendi eos rerum modi ducimus, amet libero! Soluta similique
    non sequi, pariatur saepe quod ab praesentium? Reprehenderit iusto debitis
    aliquam, omnis nobis corrupti architecto, ullam numquam et nemo ex, quas
    beatae officia consectetur nesciunt voluptates sed obcaecati explicabo
    voluptatem voluptatum alias. Aut repellat aspernatur animi amet! Autem
    consequatur iusto porro tempora iure minus molestias veritatis sapiente, ea
    quis odio ullam illo nesciunt animi aspernatur placeat mollitia! Id corrupti
    fugit dignissimos veniam, architecto possimus fuga error veritatis? Quia
    ipsa aliquam nam, nulla nihil officiis impedit architecto earum magni saepe
    deleniti molestias voluptate quis ratione corporis, fuga deserunt cumque
    amet dicta ullam. Temporibus impedit aut ullam sequi minus! Molestiae, illum
    sunt dolorem quidem nesciunt soluta ullam voluptatibus. Voluptatum numquam
    at dolores quam architecto itaque ipsam expedita eligendi incidunt ut!
    Fugit, nesciunt doloremque laborum ipsum nemo voluptatem expedita ullam.
    Praesentium pariatur cupiditate ipsa consequatur eius veniam impedit tempore
    nostrum hic debitis optio, nam molestiae voluptatum quisquam accusamus
    excepturi, temporibus saepe. Commodi quas totam laboriosam iste unde animi
    omnis distinctio!
  </p>
</template>

<style scoped lang="scss">
h2 {
  color: red;
}
p {
  color: white;
}
</style>
