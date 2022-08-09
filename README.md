<h2>Применение техники попарного тестирования на странице оформления заказа</h2>

<h4>Проанализировав форму заказа, понимаем, что можно разделить на 3 группы:</h4>
<h5>1. Санкт-Петербург<h5>
  <ul>
    <li>3 способа доставки</li>
    <li>у каждого свой метод оплаты</li>
  </ul>
  <br/ >
<img src="https://user-images.githubusercontent.com/109822424/183428167-e0197740-6587-45bc-b19a-df52ae0c453c.png" />
  
<h5>2. Кроме Санкт-Петербурга<h5>
  <ul>
    <li>Способ доставки только Пункты выдачи</li>
    <li>2 метода оплаты</li>
  </ul>
  <br/ >
<img src="https://user-images.githubusercontent.com/109822424/183428153-10919a15-b969-46c0-8e11-18e01be0be66.png" />
  
  <h5>3. Города нет в списке<h5>
  <ul>
    <li>Способ доставки только До транспортной компании</li>
    <li>2 метода оплаты</li>
  </ul>
  <br/ >
<img src="https://user-images.githubusercontent.com/109822424/183429253-4c7f80df-9048-4557-a06c-d4bb93c75921.png" />
    
    
<h4>С Санкт петербургом и городом вне списка комбинации понятны, а вот с остальными городами комбинаций много. <br />Для начала, при помощи DevTools, достанем все города:</h4>
<img src="https://user-images.githubusercontent.com/109822424/183428156-89c3e18e-9f50-48cf-9f9d-03f6995ab7e2.png" />    
    
<h4>Пропустим через https://beautifier.io для удобочитаемости</h4>    
<img src="https://user-images.githubusercontent.com/109822424/183428161-54f252c8-014b-440a-8db0-6851ac29a1e8.png" />
    
<h4>Очищаем лишнее через Coda 2 (в data-original-index разные значения, а Coda умеет подменять и такие вещи):</h4>         
<img src="https://user-images.githubusercontent.com/109822424/183428164-66b139fd-d0fc-4af1-a920-c57cbce49e2a.png" />
    
<h4>Добавляем информацию в VPTag для формирования pairwise-таблицы:</h4>      
<img src="https://user-images.githubusercontent.com/109822424/183571179-77793a12-fe7a-489b-8b0a-f5087da4d7fd.png" />

<h4>Сгенерировано 351 комбинация. Не мало. Можно подсократить список на треть, используя для физического лица в каждом городе по 1 методу оплаты. Переносим все в google-docs. Сортируем по Методу оплаты. Убираем все строки оплаты по банковской карте. </h4>
    
<img src="https://user-images.githubusercontent.com/109822424/183570861-6143a79b-0ba1-4a09-9959-bbfc251e4670.png" />
    
 <h4>В Метод оплаты для физлица чередуем значения "По квитанции в банке" / "Банковской картой". Осталось 234 комбинации.</h4>  
    
<img src="https://user-images.githubusercontent.com/109822424/183570915-f9f587ee-3eca-476f-9fcc-222feb635757.png" />
    
<h4>В Jira создаю Test-set в Xray. Прописываю шаги. Понимаю, что при клонировании меняется только заголовок и шаг с данными. Также у физического и юридического лица будут разные персональные данные. </h4>
<img src="https://user-images.githubusercontent.com/109822424/183573365-64975572-23e5-49d0-8aaf-9ce5b7cbc4c0.jpg" />

<h4>Чтобы упростить себе занесение их в Jira, готовлю в google-docs генератор заголовков для тестов и готовое значение с данными. Остается только клонировать тест и копипастить данные. Видео записано на одном экране, но на 2х мониторах это делать гораздо убоднее.</h4>

https://user-images.githubusercontent.com/109822424/183574382-080a5a46-c3a3-4286-a276-85ca19688999.mp4
    
<h4>Стираю пальцы об "Ctrl+C" "Ctrl+V"</h4> 
    
<h4>От создания первого тест-кейса до последнего прошел 1 час. <br />
Можно посмотреть на часы, в предыдущем видео было 8:47, в этом 9:40</h4>

https://user-images.githubusercontent.com/109822424/183581924-e6203d32-784f-42b0-9512-29ca1fb25b95.mp4
    
    
    
<h2>Ссылка на <a href="https://docs.google.com/spreadsheets/d/1ZwZIgC7T6C-eqRHe6fkmTg7f5sI73XItSmHHb_B4SbE/edit?usp=sharing">Google-Docs таблицу</a></h2>




    


    



  
