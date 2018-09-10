<template>
  <div class="Categories">
    <h1>Explore all TreeHouse can do for you!</h1>
    <div class="category-wrap">
      <div class="category" v-for="(category, index) in categories" :key="index">
        <span>{{category.title}}</span><br>
        <span>{{category.description}}</span><br>
        <img class="primary-img" :src="category.pic" /><br>
        <span>{{category.galleryStyles[0].title}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Categories',

  data () {
    return {
      categories: [
        {
          title: 'Bath',
          description: 'test description',
          pic: require('../assets/Icon_Bath.png'),
          galleryStyles: [
            {
              title: 'Modern Bath',
              description: 'test gallery style description',
              pic: require('../assets/Icon_Bath.png')
            },
            {
              title: 'Eclectic Bath',
              description: 'test gallery style description',
              pic: require('../assets/Icon_Bath.png')
            },
            {
              title: 'Traditional Bath',
              description: 'test gallery style description',
              pic: require('../assets/Icon_Bath.png')
            }
          ]
        },
        {
          title: 'Kitchen',
          description: 'test description 2',
          pic: require('../assets/Icon_Kitchen.png'),
          galleryStyles: [
            {
              title: 'Modern Kitchen',
              description: 'test gallery style description',
              pic: require('../assets/Icon_Kitchen.png')
            },
            {
              title: 'Eclectic Kitchen',
              description: 'test gallery style description',
              pic: require('../assets/Icon_Kitchen.png')
            },
            {
              title: 'Traditional Kitchen',
              description: 'test gallery style description',
              pic: require('../assets/Icon_Kitchen.png')
            }
          ]
        }
      ]
    }
  }

}
</script>

<style>
.Categories {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.category-wrap {
  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: space-around;
  text-align: center;
  margin: 20px;
  padding: 10px;
}
.category {
  margin: 50px;
}
.thumb {
  width: 45px;
}
.primary-img {
  width: 100%;
}

</style>
