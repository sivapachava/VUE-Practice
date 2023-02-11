<template>
    <div class="container" :class="{'show': showSidebar}">
      <div class="control">
            <i  class="fas fa-angle-double-right right-icon" @click="showNav"></i>
      </div>
      <div class="navigation-icons">
            <i class="fas fa-home home-icon"></i>
            <i class="fas fa-camera-retro home-icon"></i>
            <i class="fas fa-user-circle home-icon"></i>
            <i class="fas fa-comment-dots home-icon"></i>
            <i class="fas fa-info-circle home-icon"></i>
      </div>
    </div>
  </template>
  
  <script>
  export default {
      data: () => {
            return{
                showSidebar: false,
            }
      }
  }
  </script>
  
  <style lang="scss" scoped>
  .container {
          position: absolute;
          top:0;
          left:0;
          width: 50px;
          padding: 10px;
          min-height: calc(100vh - 20px);
          background-color: #81b181;
          border: solid #fff;
          border-width: 0 1px 0 0;
          z-index: 999;
          transition: all .5s ease-in-out;
          
          .control {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 50px;
          margin-bottom: 10px;
          .right-icon{
          font-size: 2rem;
          cursor: pointer;
          transition: all .5s ease-in-out;
           }
          }
          &.show{
              width: 180px;
          .control > right-icon{
              color:#fff;
              transform:rotateZ(-180deg);
          }
          
          }
        
        .navigation-icons{
          display: flex;
          justify-content: center;
          align-items: center;
          flex-direction: column;
          width: 50px;
          float:left;
          .home-icon{
          font-size: 2rem;
          padding: 10px 0;
          cursor: pointer;
          transition: all .5s ease-in-out;
    
          &:hover {
            color :#fff;
          }
        }
      }
    
    }
  </style>