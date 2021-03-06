# Домашнее задание №6
## Анализ корпуса текстов с помощью VoyalTools

Мной был проанализирован корпус из *11 статей про Эфиопию* в Википедии, написанных на разных языках и переведенных на английский при помощи Google Translate. Я использовала инструменты из веб-приложения **VoyantTools**. 

![image](https://user-images.githubusercontent.com/90916828/147771018-29a4087b-c812-40f4-8323-25f79226f1e1.png)

Самыми частотными словами в корпусе являются *Ethiopia (1178), Ethiopian (645), country (340), government (229), addis (200)* (видимо, как часть столицы Эфиопии, Аддис Абэбы) (слова расположены в порядке популярности их употребления). Удивительно, что слово ababa употребляется только 194 раза, так как название столицы употребляется как словосочетание, а слово Addis не было переведено как "new", чтобы оно могло быть использовано самостоятельно.

![image](https://user-images.githubusercontent.com/90916828/147770008-79bd46cc-e2f4-4c7b-b3db-7f98629d2ffe.png)

Тексты были расположены *в алфавитном порядке*. Я могу предположить, что это сделано для удобства поиска. Для каждого текста были выделены отличительные термины. **Самым длинным текстом** является статья **«eng»** с количеством слов 12793, а **самым коротким - «amh»**, с числом слов в 4349 (размер остальных статей можно посмотреть на картинке выше).

![image](https://user-images.githubusercontent.com/90916828/147770467-76f6b173-0846-487e-a190-804aa612b3d4.png)

Если разбирать частотность использованных слов, то 
- слово **«Ethiopia»** больше всего встречается в тексте **«ru»**, а меньше всего в статье с названием **«hu»**; можно заметить, что частота его использования нерегулярна;
- **«Ethiopian»** зачастую можно встретить в статье **«he»** и в наименьшем количестве в статье **«amh»**; так же, как и со словом "Ethiopia", употребление "Ethiopian" варьируется от текста к тексту;
- у **«country»** наиболее употребление наблюдается в **«no»**, а наименьшее в **«ar»**;
- **«government»** наибольшим образов в **«eng»** и наименьшим в **«amh»**;
- **«addis»** в **«ch»** и **«he»** соответственно; частотность использования "addis" отличается от текста к тексту в наименьшей степени; как и «government» не отличается большой частотой употребления по сравнению с приведенными выше словами.

Закономерно то, что слова «Ethiopia» и «Ethiopian» являются наиболее частотным, так как корпус текстов посвящен именно этой стране. Если редактировать список стоп-слов и добавить туда слова «Ethiopia» и «Ethiopian», то наиболее частотными словами становятся: country (340); government (229); addis (200); ababa (194); population (170).

Наиболее частотные слова сутя по **Scale** в каждой статье (без учета слов «Ethiopia» «Ethiopian»):
- Eng – «government», «oromo», «country»
- It - «country», «region», «government»
- Ar - «government», «country», «addis», «abeba»
- Jp - «english», «eritrea», «version»
- No - «country», «addis», «ababa»
- Amh - «country», «world», «emperor»
- Es - «music», «population», «eritrea»
- Hu - «country», «population»
- Ru - «main», «emperor», «country»
- Ch - «country», «years», «ababa», «people»
- He - «axum», «empire», «kingdom»

![image](https://user-images.githubusercontent.com/90916828/147771938-b1b555af-d43a-4faf-9ac6-a75f46f6e47b.png)

Если мы посмотрим на **Collocates**, то заметим необычность таких словосочетаний, как "ethiopia ethiopia" и "ethopia ethiopian" и тд. Скорее всего это связано с тем, что текст был переведен с языка оригинала на английский язык при помощи Google Translater, который не всегда точно передает смысл фразы. Также можно заметить, что Addis Ababa употребляется 208 раз, что странно, так как слова по отдельности употребляются 200 и 194 раза, как уже было описано выше. 

![image](https://user-images.githubusercontent.com/90916828/147773282-b4659949-652e-4594-8e20-0e45ebc26aaa.png)

Если мы посмотрим на **Correlations**, то увидим, что *употребление слов "Ethiopia" и "Ethiopian" вместе несвойственно*, что противоречит данным, полученным из **Collocates**, где такое словосочетание довольно частотно. Скорее всего, это опять же связано с трудностями перевода. Судя по показателю **Significance**, данные корреляции не значительны, так как имеют большое число. 

![image](https://user-images.githubusercontent.com/90916828/147773973-201feb04-678f-4a9d-9d30-8815e8a136ec.png)

Если мы используем инструмент **ScatterPlot**, а в анализе выберем **Document Similarity**, то мы увидим, что статьи "eng", "ar", "it", "es" наиболее похожи по употребляемым в них словам, однако сильно отличаются от статьи "amh". Остальные тексты ближе по использованным в них словам к "eng", "ar", "it", "es". 

![image](https://user-images.githubusercontent.com/90916828/147774574-d673e254-0bb4-4a72-b0f9-2b562596ceac.png)

Если же мы переключимся в анализе на "Correspondence Anaysis", то увидим, что большинство слов характерны для почти всех текстов, за исключением "amh" и "he", а слова "amharic", "emperor", "kingdom", "empire" находятся относительно далеко от всех статей приведенного корпуса.

![image](https://user-images.githubusercontent.com/90916828/147776403-8b98e4e4-14ec-46d2-9237-1fb13d114088.png)

Далее я обратилась к **DreamScape**. Видно, что наиболее часто упоминаемыми городами являются Аддис Абеба (столица Эфиопии), Аксум (скорее всего, как центр Аксумского царства и важный исторический город страны), а также Джибути, столица страны Джибути, с которой граничит Эфиопия.


