<template>
  <div id="app">
    <!-- <el-button size="medium">评论</el-button>
    <el-button size="medium" type="primary">回复</el-button> -->
    <el-badge class="item":value="1":max="9">
      <el-button nativeType="submit"></el-button>
    </el-badge>
    <el-badge class="item":value="1":max="9" isDot>
    <el-button   nativeType="medium" @click="addComment" >
        
        
      点我
    </el-button>
  </el-badge>
    <el-button :disabled="saveDisabled" @click="talk" size="small">评论</el-button>
    <el-button size="mini">前往</el-button>
    
    
    
    
  </div>
</template>

<script>
import ElBadge from '@/components/ElBadge'
import ElButton from'@/components/ElButton'
export default {
  name: 'app',
  data(){
    return{
      saveDisabled:true
    }
  },
  mounted(){
    setTimeout(()=>{
      this.saveDisabled=false
    },5000)
  },
  methods:{
    addComment(){
      console.log('点了我');
    },
    talk(){
      console.log('评论了')
    }
  },
  components: {
    ElButton,
    ElBadge
  }
}
</script>

<style>

</style>
