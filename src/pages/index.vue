<template>
  <div class="index-wrap">
    <div class="index-left">
        <div class="index-left-block">
            <template>
                <h3>{{ baQuan.title }}</h3>
                <ul>
                    <li v-for="(item,index) in baQuan.list">
                        <a :href="item.url">
                            <span class="list-index">{{ index +1 }}</span> {{ item.name }}
                        </a>
                    </li>
                </ul>
            </template>
        </div>
        <div class="index-left-block">
            <h3>{{ juChang.title }}</h3>
            <ul>
                <li v-for="(item,index) in juChang.list">
                    <a href="item.url">
                        <span class="list-index">{{ index +1 }}</span> {{ item.name }}
                    </a>
                 </li>
            </ul>
        </div>
    </div>
    <div class="index-right">
        <!-- <slide-show :slides="slides" :inv="invTime"></slide-show> -->
        <div class="index-right-list">

        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      isActive: false,
      invTime: 2000,
      slides: [
          {
            src: require('../assets/slideShow/0.jpg'),
            title: 'pic0',
            href: ''
          },
          {
            src: require('../assets/slideShow/1.jpg'),
            title: 'pic1',
            href: ''
          },
          {
            src: require('../assets/slideShow/2.jpg'),
            title: 'pic2',
            href: ''
          }
        ],
       
        baQuan: {
            title: '一月霸权',
            list: [
            {
                name: 'pop子和pipi美',
                url: ''
            },
            {
                name: '龙王的工作',
                url: ''
            },
            {
                name: 'DARLING in the FRANKXX',
                url: ''
            },
            {
                name: 'OVERLOAD',
                url: ''
            }
            ]
        },
       
       juChang: {
            title: '崩坏の剧场',
            list: [{
                name: '游戏人生ZERO',
                url: ''
            },
            {
                name: '魔法少女小圆：叛逆的物语',
                url: ''
            },
            {
                name: '凉宫春日的消失',
                url: ''
            }
         ]
       }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a,a:link{
    color: #333;
    text-decoration: none;
}

a:hover{
    color: #4fc08d;
}

.list-index{
    display: inline-block;
    color:#fff;
    background-color: #4fc08d;
    width: 16px;
    text-align: center;
    font-weight: bolder;
    border-radius: 4px;
    font-size: 13px;
    text-indent: -1px;
}

.index-wrap{
    color: #333;
    width: 100%;
}

.index-left{
    width: 220px;
    float: left;
}

.index-left-block{
    width: 200px;
    background-color: #fff;
    margin: 5px 10px;
    border-radius: 10px;
}

.index-left-block h3{
    background: #4fc08d;
    color: #fff;
    padding: 10px 15px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;    
}

.index-left-block ul {
  padding: 10px 15px;
}

.index-left-block li {
  padding: 5px;
}


</style>
