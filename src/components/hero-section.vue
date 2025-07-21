<script setup lang="js"></script>

<template>
  <header class="hero-section">
    <div class="header-top">
      <div class="top-line">
        <div class="top-line__left">
          <a href="#" class="logo">
            <img src="../assets/vue.svg" alt="logo" />
          </a>
        </div>
        <div class="top-line__center">
          <nav class="top-menu">
            <ul>
              <li class="nav__item">
                <a href="#" data-text="Хургада">Хургада</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Шарм-эль-Шейх">Шарм-эль-Шейх</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Марса-Алам">Марса-Алам</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Круизы">Круизы</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Отзывы">Отзывы</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Контакты">Контакты</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="top-line__right">
          <div class="mnu-button">
            <button class="mnu-button__menu">
              <span></span>
              <span></span>
            </button>
          </div>
          <div class="main-menu-background"></div>
          <div class="main-menu">
            <nav class="main-menu__inner">
                 <ul>
              <li class="nav__item">
                <a href="#" data-text="Хургада">Хургада</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Шарм-эль-Шейх">Шарм-эль-Шейх</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="Марса-Алам">Марса-Алам</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="">Круизы</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="">Отзывы</a>
              </li>
              <li class="nav__item">
                <a href="#" data-text="">Контакты</a>
              </li>
            </ul>
            </nav>
        </div>
      </div>
    </div>
  </div>

    <img data-speed=".8" class="hero-image" src="/egypt.png" alt="Egypt" />
    <div class="container">
      <div data-speed="1.1" class="main-header">
        <h1 class="main-title">Добро пожаловать в Египет</h1>
      </div>
    </div>
  </header>
</template>

<style lang="sass" scoped>

@import '../main.sass'

.hero-image
    width: calc( var(--index) *15 )
    position: absolute
    left: 55vw
    top: 18vh
    border-radius: 20%
    box-shadow: 100px 100px 100px rgba(0, 0, 0, 0.7)
    z-index: -1

.main-title
    font-size: calc( var(--index) *5)
    position: absolute
    width: min-content
    top: 35vh
    line-height: .9

.main-header
    height: 100vh

.header-top
    position: fixed
    top: 0
    left: 0
    right: 0
    padding-left: 30px
    padding-right: 30px
    padding-top: 20px
    pointer-events: none
    z-index: 100

.top-line
    display: flex
    gap: 50px

.top-line__left
    width: 20%
    display: flex
    align-items: center

.top-line__center
    display: flex
    justify-content: center
    flex: 1 1 0%

.top-line__right
    width: 20%
    display: flex
    gap: 5px
    justify-content: flex-end
    align-items: center

.top-menu 
    background: rgba(255, 255, 255, .5 )
    border-radius: 8px

.top-menu ul 
    display: flex
    gap: 5px

.top-menu a 
    position: relative
    font-size: 16px
    line-height: 120%
    height: 52px
    display: flex
    align-items: center
    justify-content: center
    padding: 0 20px
    border-radius: 8px
    min-width: 100px

.top-menu a::after
    position: absolute
    inset: 0
    display: flex    
    justify-content: center
    align-items: center
    background: var(--gradient-1)
    background-clip: text
    text-fill-color: transparent
    -webkit-text-fill-color: transparent
    content: attr(data-text)
    opacity: 0
    transition: var(--transition)

.top-menu a:hover::after
    opacity: .5
    


.logo, .top-menu , .mnu-button
    pointer-events: auto

</style>
