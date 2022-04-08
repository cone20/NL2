<template>
<div>
<!-- ------------------------------------- -->
<div id="card-bottom" class="card" >
    <a v-bind:href="data.link" target="_blind">
    <div class="card__product-img">
      
      <img 
        class="card__img"
        style="width:100%; height:250px;"
        alt="product-image" 
        v-bind:src="data.image"

      >
    </div>
    </a>
    <div class="card__content">
      <p class="card__name">{{ data.name }} <span v-if="data.id">#{{ data.id }}</span></p>
      <p class="card__description" v-if="data.description">{{ data.description }}</p>
      <div class="card__content-bottom">
        <div class="card__price">
          <div class="icon">
          </div>
          <p>{{ data.price }} <b><sup>$</sup></b></p>
        </div>
        <div v-if="data.stocks" class="card__time">
          <p>{{ data.stocks }} remains</p>
        </div>
      </div>
    </div>
    <div class="card__footer">
      <p class="card__autor"><span class="card__autor--alt-color">{{ data.author }}</span></p>
    </div>
  </div>


<!-- ---------------------------- -->
</div>
</template>

<script>

export default{
    name: 'Card',
    props: ["data"]
}
</script>

<style scoped lang="scss">
.icon {
  display: flex;
}
.card {
  margin-top: 0px;
  margin-bottom: 10px;
  background-color: #15263F;
  color: #b3c5df;
  border-radius: 16px;
  padding: 24px;
  max-width: 295px;
  font-size: 1.5rem;
  box-shadow: 0 25px 50px 0 rgba(153, 20, 20, 0.1);
  @media screen and (min-width: 768px) {
    font-size: 1.6rem;
    width: 350px;
    padding-bottom: 32px;
  }
  .card__product-img {
    cursor: pointer;
    position: relative;
    border-radius: 8px;
    overflow: hidden;
    @mixin hoverOpacity {
      content: "";
      position: absolute;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0;
      transition: opacity 0.25s ease-out;
    }
    &::before {
      @include hoverOpacity;
      background-color: cyan;
    }
    &::after {
      @include hoverOpacity;
    }
    &:hover {
      &::before {
        opacity: 0.5;
      }
      &::after {
        opacity: 1;
      }
    }
  }
  .card__content {
    display: flex;
    flex-direction: column;
    gap: 12px;
    padding: 16px 0 16px 0;
    @media screen and (min-width: 768px) {
      gap: 16px;
      padding: 24px 0;
    }
    .card__name {
      color: white;
      font-size: 20px;
      font-weight: bold;
      cursor: pointer;
      &:hover {
        color: #00FFF8;
      }
    }
    .card__description {
      font-size: 16px;
      
      text-align: justify;
    }
    .card__time{
        font-size: 17px;
    }
    .card__content-bottom {
      display: flex;
      justify-content: space-between;
      padding-top: 4px;
      @media screen and (min-width: 768px) {
        padding-top: 6px;
      }
      > * {
        display: flex;
        align-items: center;
        gap: 8px;
        font-weight: 600;
      }
      .card__price {
        color: #00FFF8;
        font-size: 17px;
        font-weight: 800;
      }
    }
  }
  .card__footer {
    align-items: center;
    border-top: 1px solid #2E405A;
    font-size: 18px;
    text-align: center;
    font-weight: 800;
    margin-bottom: -20px;
    .card__autor--alt-color {
      color: white;
      cursor: pointer;
      &:hover {
        color: #00FFF8;
      }
    }
    .card__autor{
      margin-top: 15px;
    }
  }
}

@media (max-width: 1200px){
  .card:last-child{
  text-align: center;
  width:100%;
  }

}



//Transition
.fade-enter-active,
.fade-leave-active {
    transition: 0.25s ease-out;
}
.fade-leave-to,
.fade-enter-from {
  opacity: 0;
}
</style>
