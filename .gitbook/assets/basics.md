# Основа

Просто друкувати "hello world" недостатньо, чи не так? Ви хочете зробити більше, ніж це ви хочете ввести щось, маніпулювати ним і що-небудь зробити. Ми можемо досягти цього в Python, використовуючи константи і змінні, і ми дізнаємося деякі інші поняття, а також в цій главі.

## Коментарі

_Comments_-це будь-який текст праворуч від символу ' # ' і в основному корисний в якості заміток для читача програми.

Для прикладу:

або:

```python
#  Нотатка про те що друкує ця функція
print('hello world')
```
Використовуйте якомога більше корисних коментарів в програмі, щоб:


- пояснити припущення
- пояснити важливі рішення
- пояснити важливі деталі
- пояснити проблеми, які ви намагаєтеся вирішити
- пояснити проблеми, які ви намагаєтеся подолати в своїй програмі і т. д.

[*Код говорить вам, як, коментарі повинні сказати вам, чому*][*Code tells you how, comments should tell you why*](http://www.codinghorror.com/blog/2006/12/code-tells-you-how-comments-tell-you-why.html).

Це корисно для читачів вашої програми, щоб вони могли легко зрозуміти, що робить програма. Пам'ятайте, що цією людиною можете бути Ви самі через півроку!


## Литеральные Константи


Прикладом літеральной константи є числa типу "5", " 1.23" або рядок типу "це рядок" або " це рядок!".

Він називається літералом, тому що це _literal_ - ви використовуєте його значення буквально. Число " 2 " завжди представляє себе і нічого більше - це _constant_, тому що його значення не може бути змінено. Отже, всі вони називаються константами.


## Числа

Числа в основному бувають двох типів-цілі і з плаваючою комою (не цілі, "3.14").

Прикладом цілого числа є "2", яке є просто цілим числом.

Прикладами чисел з плаваючою комою (або _floats_ для стислості) є `3.23` і `52.3 E-4`. Позначення " E " вказує на ступені 10. В цьому випадку `52.3 E-4` означає `52.3 * 10^-4^`.

> * * Примітка Для досвідчених програмістів**

> Немає окремого "long" типу. Тип ' int ' може бути цілим числом будь-якого розміру.

## Стрічки


Рядок (string) - це _sequence_ of _characters_ (набір букв). Рядки в основному просто купа слів.

Ви будете використовувати рядки майже в кожній програмі Python, яку ви пишете, тому зверніть увагу на наступну частину.

### одинарні лапка


Ви можете вказати рядки, використовуючи одинарні лапки 'такі як Quote me on this'.

Всі прогалини (пробіли), тобто прогалини і таби, в лапках, зберігаються як є.

### подвійні лапки

Рядки в подвійних лапках працюють точно так само, як рядки в одинарних лапках. Наприклад `"як тебе звуть?"`.

### Потрійні лапки {#triple-quotes}

Ви можете вказати багаторядкові рядки, використовуючи потрійні лапки-(`"""`або`'''`). Ви можете використовувати одинарні лапки і подвійні лапки вільно в потрійних лапках. Приклад:

```python
'''Це багаторядковий рядок. Це перший рядок.
Це другий.
"Як тебе звати?" - Запитав я.
Він сказав: "Бонд, Джеймс Бонд."
'''
```
### Рядки Незмінні


Це означає, що після того, як ви створили рядок, ви не можете змінити його. Хоча це може здатися
поганим, але це не так. Ми побачимо, чому це не є обмеженням в різних програмах, які
побачимо пізніше.

> * * Примітка для програмістів C / C++ **
> 
> В Python немає окремого типу даних "char". У цьому немає необхідності, і я впевнений, що ви не сумуватимете за ним.

<!-- -->

> * * Примітка для програмістів Perl / PHP**
> 
> Пам'ятайте, що рядки в одинарних і подвійних лапках однакові-вони нічим не відрізняються.

### Метод format


Іноді ми можемо захотіти побудувати рядки з іншої інформації. Тут корисний метод format ().

Збережіть наступні рядки у вигляді файлу str_format.py`:

```python
age = 20
name = 'Swaroop'

print('{0} було {1} років  коли він написав цю книгу'.format(name, age))
print('Чому {0} грається з тим Python?'.format(name))
```

Вихід:

```
$ python str_format.py
Swaroop було 20 років коли він написав цю книгу
Чому Swaroop грається з тим  Python?
```
** Як Це Працює**

Рядок може використовувати певні специфікації, а потім метод "format" може бути викликаний для заміни цих специфікацій відповідними аргументами методу "format".

Зверніть увагу на перше використання, де ми використовуємо " {0}", і це відповідає змінної "name", яка є першим аргументом методу format. Аналогічно, друга Специфікація '{1}' відповідає 'віку', який є другим аргументом методу format. Зверніть увагу, що Python починає відлік з 0, що означає, що перша позиція має індекс 0, друга позиція має індекс 1, і так далі.

Зверніть увагу, що ми могли б досягти того ж за допомогою конкатенації рядків:

```python
name + ' має ' + str(age) + ' років'
```
але це набагато потворніше і більше щансів отримати помилку. По-друге, перетворення в рядок буде виконуватися автоматично методом "format" замість явного перетворення рядка, необхідного в цьому випадку. По-третє, при використанні методу "format" ми можемо змінити повідомлення без необхідності мати справу з використовуваними змінними і навпаки.

Також зверніть увагу, що числа є необов'язковими, тому ви могли б також написати:

```python
age = 20
name = 'Swaroop'

print('{} було {} років  коли він написав цю книгу'.format(name, age))
print('Чому {} грається з тим Python?'.format(name))
```
що дасть той самий результат, що і попередня програма.

Ми також можемо назвати параметри:

```python
age = 20
name = 'Swaroop'

print('{name} було {age} років  коли він написав цю книгу'.format(name=name, age=age))
print('Чому {name} грається з тим Python?'.format(name=name))
```

що дасть той самий точний результат, що і попередня програма.

Python 3.6 представив коротший спосіб виконання іменованих параметрів, званих " F-рядками"("f-strings"):

```python
age = 20
name = 'Swaroop'

print(f'{name} було {age} років  коли він написав цю книгу'.format(name, age)) # зверніть увагу на 'f' перед рядком
print(f'Чому {name} грається з тим Python?'.format(name)) # зверніть увагу на 'f' перед рядком
```

що дасть той самий точний результат, що і попередня програма.


Те, що Python робить у методі "format", полягає в тому, що він замінює кожне значення аргументу на місце специфікації. Можуть бути більш детальні специфікації такі як:

```python
# десяткове число (.) точність 3 для float '0.333'
print ('{0:.3f}'.farmat(1.0/3))
# заповнити підкресленнями (_) з текстом по центру
# ( ^ ) до 11 width'___hello___'
frint('{0:_^11}'.format('hello'))
# на основі ключових слів "Swaroop написав A Byte of Python"
print('{name} написав {book}'.format(ім'я= 'Swaroop', книга= 'A Byte of Python'))
```

Вивід:

```
0.333
___hello___
Swaroop написав A Byte of Python
```

Оскільки ми обговорюємо форматування, зверніть увагу, що "print" завжди закінчується невидимим символом "нового рядка" ("\n"), так що повторні виклики "друку" будуть друкуватися на окремому рядку кожен. Щоб цей символ нового рядка не друкувався, можна вказати, що він повинен закінчуватись пробілом:

```python
print('a', end='')
print('b', end='')
```

Вивід:

```
ab
```

Або ви можете "закінчити" пробілом:

```python
print('a', end=' ')
print('b', end=' ')
print('c')
```
Виведеться ось це:

```
a b c
```

### escape-послідовність


Припустимо, ви хочете мати рядок, що містить одну лапку ( ' ), як ви вкажете цей рядок? Наприклад, рядок `"як тебе звуть?"`. Ви не можете вказати 'What's your name?' тому що Python буде плутати, де починається і закінчується рядок. Таким чином, вам треба буде вказати, що ця одинарна лапка не вказує на кінець рядка. Це можна зробити за допомогою того, що називається _escape sequence_. Вказати одинарну лапку як "\'" : зверніть увагу на зворотну косу риску. Тепер ви можете вказати рядок як 'What\'s your name?'.

Інший спосіб вказати цей конкретний рядок `"What's your name?"`тобто використовуючи подвійні лапки. Аналогічно, ви повинні використовувати escape-послідовність для використання подвійної лапки в рядку з подвійними лапками. Крім того, ви повинні вказати зворотну косу риску перед зворотньою косою рискою, використовуючи escape-послідовність `\\`.

Що робити, якщо ви хочете вказати дворядковий рядок? Один із способів-використовувати рядок у потрійних лапках, як показано [раніше] (#triple-quotes), або ви можете використовувати escape - послідовність для символу нового рядка `\n`, щоб вказати початок нового рядка. Приклад:

```python
'Це перший рядок\nЦе другий рядок'
```

Іншою корисною Escape-послідовністю є Таб: '\ t'. Є ще багато escape-послідовностей, але я згадав тільки самі корисні.

Слід зазначити, що в рядку одна зворотна коса риса в кінці рядка вказує, що рядок триває в наступному рядку, але новий рядок не додається. Наприклад:

```python
"Це перше речення. \
Це друге речення."
```
Є рівним до

```python
"Це перше речення.Це друге речення."
```
### Необроблений Рядок

Якщо вам потрібно вказати деякі рядки, де не обробляються спеціальні обробки, такі як escape-послідовності, то вам потрібно вказати рядок _raw_, додавши префікс " r " або " R " до рядка. Приклад:

```python
r"нові рядки позначаються \n"
```

> * * Примітка Для користувачів регулярних виразів**
> 
> Завжди використовуйте необроблені рядки при роботі з регулярними виразами. В іншому випадку може знадобитися багато "backwhacking". Наприклад, зворотні посилання можуть називатися `'\\1'` або `r'\1'`.

## Змінні


Використання тільки літеральних констант скоро може стати нудним - нам потрібен якийсь спосіб зберігання будь-якої інформації і маніпулювання нею. Ось тут-то і з'являються змінні. Змінні - це саме те, про що говорить їх назва - їх значення може змінюватися, тобто ви можете зберігати що завгодно, використовуючи змінну. Змінні - це просто частини пам'яті вашого комп'юте ра, де ви зберігаєте деяку інформацію. На відміну від літеральних констант, вам потрібен якийсь метод доступу до цих змінних і, отже, ви даєте їм імена.

## Identifier Naming## Іменування Ідентифікаторів


Змінні є прикладами ідентифікаторів. _Identifiers_-імена, дані для ідентифікації чогось. Є кілька правил, яким ви повинні слідувати для іменування ідентифікаторів:


- Першим символом ідентифікатора повинна бути буква алфавіту (верхній або нижній регістр ASCII або символ Юнікоду) або символ підкреслення (`_`).
- Інша частина імені ідентифікатора може складатися з букв (верхній регістр ASCII або нижній регістр ASCII або символ Юнікоду), підкреслення ( ` _ ' ) або цифр (0-9).
- Імена ідентифікаторів чутливі до регістру. Наприклад, "myname" і "myName" - це не одне й те саме. Зверніть увагу на нижній регістр " n "в першому і верхній регістр" N " у другому.
- Приклади _дійсних, валідних_ імен ідентифікаторів `i`, `name_2_3`. Приклади _невалідних, недійсних_ імен ідентифікаторів - `2things`, `this is spaced out`, `my-name` and `>a1b2_c3`.


## Тип даних

Змінні можуть містити значення різних типів, званих _data types_(_типи данних_). Основними типами є числа і рядки, про які ми вже говорили. У наступних розділах ми побачимо, як створювати власні типи за допомогою [класів] (./oop.md#classes).
## Об'єкт


Пам'ятайте, Python відноситься до всього, що використовується в програмі як до _обєктів_.  Це мається на увазі в загальному сенсі. Замість того щоб говорити "щось", ми говоримо "об'єкт".


> **Примітка для користувачів об'єктно-орієнтованого програмування **:
>
> Python строго об'єктно-орієнтований в тому сенсі, що все є об'єктом, включаючи числа, рядки і функції.


Зараз ми побачимо, як використовувати змінні з константами. Збережіть такий приклад і запустіть програму.

## Як писати програми на Python

Далі стандартна процедура, щоб зберегти і запустити програму на мові Python наступним чином:

### Для PyCharm

1. Відкрити [PyCharm] (./first_steps.md#pycharm).
2. Створіть новий файл із зазначеним ім'ям файлу.
3. Введіть код програми, наведений у Прикладі.
4. Клацніть правою кнопкою миші та запустіть поточний файл.


Примітка: всякий раз, коли ви повинні надати [аргументи командного рядка](./modules.md#modules), натисніть `Виконати` - > `змінити конфігурації` (`Run` -> `Edit Configurations`) і введіть аргументи в розділі "Параметри скрипта:" (`Script parameters:`) та натисніть кнопку `ОК`:




![аргументи командного рядка PyCharm](./img/pycharm_command_line_arguments.png)


### Для інших редакторів


1. Відкрийте редактор за вашим вибором.
2. Введіть код програми, наведений у Прикладі.
3. Збережіть його у вигляді файлу з вказаним ім'ям файлу.
4. Запустіть інтерпретатор за допомогою команди `python program.py` щоб запустити програму.

### Приклад: Використання Змінних І Констант

Введіть і запустіть наступну програму:


```python
# імя файлу : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''Це багато рядкова стрічка.
Це другий рядок.'''
print(s)
```

Вивід:

```
5
6
Це багато рядкова стрічка.
Це другий рядок.
```

** Як Це Працює**

Ось як працює ця програма. По-перше, ми присвоюємо літеральне постійне значення `5` змінної `i` за допомогою оператора присвоювання (`=`). Цей рядок називається оператором, тому що він стверджує, що щось має бути зроблено, і в цьому випадку ми пов'язуємо ім'я змінної `i` зі значенням `5`. Потім ми друкуємо значення `i`, використовуючи оператор `print`, який, як не дивно, просто виводить значення змінної на екран.

Потім ми додаємо `1` до значення, що зберігається в `i`, і зберігаємо його назад. Потім ми друкуємо його і очікувано отримуємо значення `6`.

Аналогічним чином, ми присвоюємо Рядкове значення змінної `S` і потім роздруковуємо його.

> ** Примітка для програмістів на статичних мовах**
> 
> Змінні використовуються, просто присвоївши їм значення. Оголошення або визначення типу даних не потрібно / не використовується.

## Логічна І Фізична Лінія

Фізичний рядок-це те, що ви бачите, коли пишете програму. Логічний рядок - це те, що бачить _python_ як одне твердження. Python неявно припускає, що кожен _фізичний рядок_ відповідає _логічному рядку_.


Прикладом логічного рядка є оператор типу `print ('hello world')` - якщо це в рядку саме по собі (як ви бачите в редакторі), то це також відповідає фізичної рядку.


Неявно Python заохочує використання одного оператора на рядок, що робить код більш читаним.

Якщо ви хочете вказати кілька логічних рядків в одному фізичному рядку, ви повинні явно вказати це за допомогою точки з комою (`;`), яка вказує на кінець логічного рядка / оператора. Наприклад:


```python
i = 5
print(i)
```


одним і тим самим що і

```python
i = 5;
print(i);
```
що у свою чергу ж тим самим що і

```python
i = 5; print(i);
```
і тим самим що

```python
i = 5; print(i)
```

Проте, я * наполеглево рекомендую * дотримуватися * запис максимум одного логічного рядка на кожному окремому фізичному рядку*. Ідея полягає в тому, що ви ніколи не повинні використовувати крапку з комою. Насправді, я ніколи не використовував цього знку або навіть не бачив крапки з комою в програмі Python.

Існує одна ситуація, коли ця концепція дійсно корисна: якщо у вас є довгий рядок коду, Ви можете розбити його на кілька фізичних рядків за допомогою риски. Це називається _explicit line joining_:


```python
s = 'Це стрічка. \
Це продовження стрічки.'
print(s)
```

Вивід:

```
Це стрічка. Це продовження стрічки.
```

Подібно

```python
i = \
5
```
є тим самим що і

```python
i = 5
```

Іноді існує неявне припущення, що вам не потрібно використовувати зворотну косу риску. Це той випадок, коли в логічному рядку є дужки, квадратні дужки або фігурні дужки. Це називається *неявне з'єднання рядків*. Ви можете побачити це в дії, коли ми пишемо програми за допомогою [списку](./data_structures.md#lists) в наступних розділах.

## Поглиблення


Пробіли важливі в Python. Насправді, * пробіли на початку рядка важливі*. Це називається _indentation_. Початкові пробіли (пробіли і табуляція) на початку логічного рядка використовуються для визначення рівня відступу логічного рядка, який в свою чергу використовується для визначення угруповання операторів.


Це означає, що заяви, які йдуть разом _повинні_ мати однаковий відступ. Кожен такий набір операторів називається блоком. Приклади того, як важливі блоки, ми побачимо в наступних главах.

Одна річ, яку Ви повинні пам'ятати, що неправильний відступ може призвести до помилок. Наприклад:


```python
i = 5
# Помилка нижче! Зверніть увагу на пробіл на початку рядка
 print('Value is', i)
print('Я повторюю, значення ', i)
```

При запуску цього з'являється таке повідомлення про помилку:

```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```

Зверніть увагу, що на початку другого рядка є один пробіл. Помилка, зазначена Python говорить нам, що синтаксис програми є неприпустимим, тобто програма не була правильно написана. Це означає, що ви не можете довільно запускати нові блоки тверджень (за винятком основного блоку за замовчуванням, який ви використовували весь час, звичайно). Випадки, коли ви можете використовувати нові блоки, будуть детально описані в наступних розділах, таких як [потік управління](./control_flow.md#control_flow).


> * * Як відступати**
> 
> Використовуйте чотири пробіли для відступу. Це офіційна рекомендація мови Python. Хороші редактори автоматично зроблять це за вас. Переконайтеся, що ви використовуєте однакову кількість пробілів для відступів, інакше програма не буде запущена або матиме несподівану поведінку.


<!-- -->



> * * Примітка для програмістів які використовують статичної мови**
> 
> Python завжди буде використовувати відступи для блоків і ніколи не буде використовувати дужки. Запустіть 
> Python will always use indentation for blocks and will never use braces. Run `from __future__ import braces`, щоб дізнатися більше.

## Резюме


Тепер, коли ми пройшли через безліч дрібних деталей, ми можемо перейти до більш цікавих речей, таких як оператори потоку управління. Переконайтеся, що ви освоїлися з тим, що прочитали в цьому розділі.