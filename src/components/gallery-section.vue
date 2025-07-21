<script setup lang="js">


</script>

<template>
 

            <div class="gallery__section">
    <div class="container">
        <div class="gallery">
            <div data-speed=".85" class="gallery__left">
                <img  class="gallery__item" src="/ras-mohhamed.jpg" alt="">
                <img  class="gallery__item" src="/ras1.jpg" alt="">

             <div class="text-block gallery__item">
                    <h2 class="text-block__h">
                        Рассвет в пустыне + сафари на квадроциклах или багги (всё включено)
                        
                    </h2>
                    <p class="text-block__p">
                       Сафари на рассвете — всегда хорошая идея!
                        На улице в это время не жарко, можно с комфортом кататься и гулять, а восход солнца в пустыне просто завораживает.
                         Наш путь будет пролегать через деревню бедуинов, к которым мы обязательно заедем в гости.
                          Вы попробуете традиционный чай кочевников и познакомитесь с их бытом.
                           А после экскурсии мы отвезём вас в отель прямо к завтраку.
                       
                    </p>
                </div>
                <img  class="gallery__item" src="/kv.png" alt="">
                 <img  class="gallery__item" src="/petra1.jpg" alt="">
                <img  class="gallery__item" src="/petra2.jpg" alt="">
            </div>

                
            <div data-speed="1" class="gallery__right">
                <div class="text-block gallery__item">
                    <h2 class="text-block__h">
                        Египетские Мальдивы — дайвинг и снорклинг в Рас Мохаммеде
                    </h2>
                    <p class="text-block__p">
                        Вы любите дайвинг и снорклинг? А возможно вы только знакомитесь
                        с подводным миром? Тогда эта экскурсия для вас.
                        Со мной вы отправитесь в заповедную зону Рас-Мохаммед. 
                        Это идеальное место для подводного плавания. 
                        В течение дня мы сделаем 3 остановки, в том числе посетим Белый остров! 
                    </p>
                </div>
                <img  class="gallery__item" src="/ras2.jpg" alt="">
                <img  class="gallery__item" src="/kv2.png" alt="">
                <img  class="gallery__item" src="/kv3.png" alt="">
                  <div class="text-block gallery__item">
                    <h2 class="text-block__h">
                       В Петру на пароме из Шарм-эль-Шейха
                        
                          
                    </h2>
                    <p class="text-block__p">
                        Предлагаем вам побывать в таинственной Петре — древнем городе, хранящем множество легенд и исторических загадок.
                         Вы увидите, как невероятный природный объект благодаря стараниям человека стал шедевром архитектуры, скрытым среди розово-красных скал. 
                        
                    </p>
                </div>
                 <img  class="gallery__item" src="/petra3.jpg" alt="">
            </div>
        </div>
    </div>
</div>
       
</template>


<style lang="sass" scoped>

@import '../main.sass'


.gallery
    display: flex
    padding: calc( var(--index) * 10 ) 

.gallery > * 
    flex: 1
    display: flex
    align-items: center
    flex-direction: column

.gallery__item
    width: calc( var(--index) * 17.5 )
    margin-bottom: var(--gallery-gap)
    max-height: 100vh
    border-radius: 25px

.gallery__left 
    margin-top: calc( var(--gallery-gap) *2  )

.gallery__right 
    margin-top: calc( var(--gallery-gap) *1 )
   

.text-block
    color: var(--color-text)
    position: relative
    
.text-block__h
    font-size: 3rem
    line-height: 2.8rem
    color: var(--color-header)
    margin-bottom: 2rem

.text-block__p
    line-height: 1.5rem

</style>