## Структурна лінгвістика

### 1. Побудуйте ланцюжок походження слів за зразком:

оженитися: (о + (женити + ся))

1. несприйнятливість (не (сприйнят + ливість))
2. атиповий (а + (тип + овий))
3. безвідповідально (без (відповід + ально))
4. мореплавання (море + плавання)
5. оподаткувати (о + (податк + увати))
6. перевтілитися (пере + ((втіл + ити) + ся))
7. схилившись (с + ((хили + в) + шись))
8. трьохярусний (трьох + (ярус + ний))
9. підсніжник (під + (сніж + ник))
10. зужиткований (з + (ужитк + ований))

### 2. Перевірте роботу [SnowballStem](http://snowballstem.org/) для спільнокореневих слів. Напишіть ваші спостереження.

```
$ stack build && stack exec snowball-stem
> Analyzing: truth, truthful, truthfulness, countertruth, untruthful, truthology
truth, truth, truth, countertruth, untruth, trutholog
> Analyzing: flaw, flaws, flawed, flawless, flawlessness, flawlessly
flaw, flaw, flaw, flawless, flawless, flawless
> Analyzing: лес, лесной, лесник, лесничий, лесничество, пролесье
лес, лесн, лесник, леснич, лесничеств, пролес
> Analyzing: окно, окошко, подоконник, оконный, окнище
окн, окошк, подоконник, окон, окнищ
```

(code is available at https://github.com/k-bx/nlp/tree/master/snowball-stem )

Спостереження:

- не розпізнався derivational affix (prefix) "counter" в словах
  "countertruth", "untruthful"
- не розпізнався суфікс "-ology" в "truthology", "-less" в "flawless",
  "flawlessness" та "flawlessly"
- суфікс "-ной" не повністю відрізався в "лесной", неправильно
  відрізано "-чий" в "лесничий" (треба в "лесник" або вже "лес"),
  "-чество" в "лесницество", префікс "про-" в "пролесье"
- аналогічно з "окно"м, все погано

### 3. Визначте частину мови виділеного слова і зв'язок до його батька (за зразком):

1. We can {but} hope that everything will be fine.: coordinating conjunction cc(can, but)
2. It's sad {but} true.: coordinating conjunction cc(sad, but)
3. Jack brings nothing {but} trouble.: adposition preposition(nothing, but)
4. {As} we were talking, I realised how to solve the issue.: adposition marker(talking, as)
5. This hot dog isn't {as} big as usual.: adverb advmod(big, as)
6. This hot dog isn't as big {as} usual.: adposition prepositionr(big, as)
7. This hot dog isn't as big {as} I expected: adposition marker(expected, as)
8. I work {as} a teacher.: adposition preposition(as, teacher)
9. Let's do it this {way}!: noun npadvmod(do, way)
10. This is {way} too much!: adverb advmod(is, much)
11. The prices are going {down}.: particle prt(going, down)
12. Someone pushed him and he fell {down} the stairs.: adposition preposition(fell, down)
13. I’ve been feeling rather {down} lately.: adverb advmod(feeling, down)
14. It's not easy to {down} a cup of coffee in one gulp.: verb xcomp('s, down)
15. Bring a {down} jacket and a pair of gloves, and you'll be fine.: adjective amod(jacket, down)

### 4. Визначте частину мови виділеного слова, його лему і зв'язок до його батька (за зразком):

{Я} люблю черепашок.: займенник, я, nsubj(люблю, Я)  
Я {люблю} черепашок.: дієслово, любити, root(ROOT, люблю)  
Я люблю {черепашок}.: іменник, черепашка, dobj(люблю, черепашок)  

1. Рада міністрів Європейського союзу затвердила угоду про спрощений порядок видачі {віз} для України. : іменник, віза, nmod(видачі, віз)
2. Батько Себастьяна {віз} на санях їх театральний гурт до Львова. : дієслово, возити, root(віз)
3. А ще дивний елемент інтер’єру – {віз} із продукцією одного з херсонських виробників. : іменник, віз, root(віз)
4. У цю мить {повз} Євгена пролетів останній вагон товарняка. : прийменник, повз, pcomp(мить,повз)
5. Кліпнув очима і побачив малого песика, який саме пробігав {повз} у бік села. : прийменник, повз, prep(пробігав, повз)
6. Степанко перестав кричати, тільки ламкий стогін {повз} йому із грудей. : дієслово, повзти, root(повзти)
7. Часу не {гай} – декларацію подай! : дієслово, гаяти, root(гаяти)
8. І коляд заспівали, і {гай} врятували. : іменник, гай, nmod(врятувати, гай)
9. {Гай}, чи ви забулися, братове? : вигук, гай, intj(забулися, гай)
10. Ось присіла на {край} ліжка. : іменник, край, pobj(на, край)
11. Поставив ту кузню не {край} дороги, як було заведено, а на Красній горі, біля Прадуба. : прийменник, край, prep(кузню, край)
12. Розповідаючи про передній {край} лінґвістики, фон Лібіх, як завжди, мислив широко і глобально. : іменник, край, root(край)
13. Не {край} мені серце. : дієслово, краяти, root(краяти)
14. І {щойно} тоді додаємо до борщу смажену цибулю. : частка, щойно, partmod(тоді, щойно)
15. Бо {щойно} я задрімав, віддавши тіло подушці з периною, як мене розбудив поштовх у бік. : прислівник, щойно, advmod(задрімав, щойно)

### 5. Побудуйте синтаксичну структуру речень за зразком:

Я люблю черепашок.  
nsubj(люблю, Я)  
root(ROOT, люблю)  
dobj(люблю, черепашок)

1. Пригадую, уже згодом, коли я відбував свій термін у таборі № 36 у Кучино Пермської області, я отримав від Михасі листівку з жартівливим описом того, як Київ готується до святкування свого 1500-ліття.

root(пригадую)
advmod(пригадую, уже)
advmod(пригадую, згодом)
advmod(пригадую, коли)
nsubj(відбував, я)
xcomp(пригадую, відбував)
poss(термін, свій)
prep(відбував, у)
pobj(у, таборі)
npadvmod(відбував, №36)
prep(таборі, у)
pobj(у, Кучино)
poss(області, Пермської)
poss(Кучино, області)
nsubj(отримав, я)
conj(отримав)
prep(отримав, від)
pobj(від, Михасі)
dobj(отримав, листівку)
prep(листівку, з)
advmod(описом, жартівливим)
pobj(з, описом)
pobj(описом, того)
advmod(Київ, як)
verb(готується, Київ)
conj(готується)
prep(готується, до)
pobj(до, святкування)
poss(1500-ліття, свого)
advmod(святкування, 1500-ліття)

2. 6C приземляється на плече, перекочуючись, пролітає метрів п’ятдесят і витягується на снігу за кілька кроків від забризканої палаючими уламками посадкової смуги.

nsubj(6С)
root(приземляється)
prep(приземляється, на)
pobj(на, плече)
advcl(приземляється, перекочуючись)
conj(приземляється, пролітає)
npadvmod(пролітає, метрів)
nummod(метрів, п'ятдесят)
cconj(пролітає, і)
conj(пролітає, витягується)
prep(витягується, на)
pobj(на, снігу)
prep(витягується, за)
amod(кроків, кілька)
pobj(за, кроків)
prep(кроків, від)
amod(смуги, забризканої)
amod(уламками, палаючими)
pobj(забризканої, уламками)
amod(смуги, посадкової)
pobj(від, смуги)

3. Дівчина стояла там, де й була, і намагалася привести до ладу скуйовджене волосся, вкрай розлючена тим, що це побачили водії, які чекали на переїзді.

nsubj(стояла, дівчина)
root(стояла)
advmod(стояла, там)
advmod(була, де)
advmod(була, й)
advcl(стояла, була)
cc(стояла, і)
conj(стояла, намагалася)
pobj(намагалася, привести)
aux(ладу, до)
comp(намагалася, ладу)
poss(волосся, скуйовджене)
dobj(привести, волосся)
advmod(розлючена, вкрай)
advcl(привести, розлючена)
prep(розлючена, тим)
mark(побачили, що)
nsubjpass(побачили, це)
conj(розлючена, побачили)
nsubj(побачили, водії)
nsubj(водії, які)
relcl(водії, чекали)
prep(чекали, на)
pobj(на, переїзді)

### 6. Виберіть одне cлово зі списку та побудуйте лексико-семантичні зв'язки до трьох різних значень цього слова. Фактично, потрібно побудувати WordNet-подібні вузли. Значення слів можна перевірити у [СУМі](http://sum.in.ua/) та [Словниках України](http://lcorp.ulif.org.ua/dictua/).

Слова на вибір: вік, стіна, добро, серце, центр, куля, міст, ланцюг, бік, дух.

Слово Міст:

- Те, що є проміжним між чим-небудь, що з'єднує щось:
  - hypernyms: об'єднання, сполучення
  - sister terms: перегін, стежка
  - hyponyms: канатна дорога, трап
  - meronyms: балка, свая
- Положення тіла з вигнутою догори грудною кліткою і з упором на долоні й п'яти:
  - hypernyms: поза, положення, стан
  - sister terms: планка
  - hyponyms: -
  - meronyms: -
- Частина шасі автомашини, трактора
  - hypernyms: деталь, трактор, автомашина
  - sister terms: -
  - hyponyms: -
  - meronyms: -