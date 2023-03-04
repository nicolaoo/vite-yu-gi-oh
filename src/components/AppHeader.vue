<script >
export default {
  data() {
    return {

    }
  }
}

</script>

<template>
  <header>
    <div class="container">
      <div class="row-title">
        <figure>
          <img
            src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg/260px-Yu-Gi-Oh%21_%28Logo%29.jpg"
            alt="">
        </figure>
        <h1>
          yu-gi-yo
        </h1>
      </div>
    </div>
  </header>
</template>
 
<style lang="scss" scoped>
header {
  background-image: url('https://fs-prod-cdn.nintendo-europe.com/media/images/10_share_images/games_15/nintendo_switch_download_software_1/H2x1_NSwitchDS_YuGiOhRushDuelDawnOfTheBattleRoyale_image1280w.jpg');
  aspect-ratio: 20/4;
  object-position: top;
}

.row-title {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  padding: 10px 0;

  figure {
    flex-basis: 30%;


    img {
      border-radius: 20px;
    }
  }

  h1 {
    flex-basis: auto;
  }

}
</style>
