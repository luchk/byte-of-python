#Про Python

Python є однією з тих рідкісних мов, які можуть бути в одночас і _simple_ і _powerful_ (_простою_ і _потужною_).  Ви будете приємно здивовані, побачивши, як легко зосередитися на вирішенні проблеми, а не на синтаксисі і структурі мови, на якій ви програмуєте.

Офіційне введення в Python:

> Python - це проса в освоєнні, потужна мова програмування. Вона має ефективні структури даних високого рівня і простий, але ефективний підхід до об'єктно-орієнтованого програмування. Елегантний синтаксис і динамічну типізацію, разом з його інтерпритованістю роблять його ідеальним мовою для скриптів та швидкої розробки додатків у багатьох областях на більшості платформ.

Я більш детально розгляну більшість з цих функцій у наступному розділі.

## Історія саме такої назви

Гвідо ван Россум (Guido van Rossum), творець мови Python, назвав мову у честь шоу Бі-бі-сі (BBC) "Монті Літаючий цирк пітона" ("Monty Python's Flying Circus"). Він не особливо любить змій, які вбивають тварин для їжі, намотуючи свої довгі тіла навколо них і розтрощуючи їх.

## Особливості Python

### Простий (простота)

Python це проста і мінімалістична мова. Читаючи хорошу програму на Python, Ви відчуває себе майже так само: ніби Ви читаєте щось англійською, хоча і дуже суворою Англійською! Це характер псевдо-коду Python є одним з його найбільших достоїнств. Це дозволяє зосередитися на вирішенні проблеми, а не на самій мові.

### Легкий у вивчені

Як ви побачите, почати роботу з Python надзвичайно легко. Python має дуже простий синтаксис, як вже згадувалося.

### Безкоштовно і з відкритим вихідним кодом


Python є прикладом _FLOSS_ (Free/Libre і Open Source Software)  (Безкоштовний/вільний і з відкритим вихідним кодом). Простіше кажучи, ви можете вільно поширювати копії цього програмного забезпечення, читати вихідний код, вносити в нього зміни і використовувати його частини в нових безкоштовних програмах. FLOSS заснована на концепції спільноти, яка розділяє знання. Це одна з причин, чому Python настільки гарний - він був створений і постійно вдосконалюється спільнотою, яка просто хоче бачити кращий Python.


### Мова високого рівня (Високорівнева мова)


Коли ви пишете Програми на Python, вам ніколи не потрібно турбуватися про низькорівневі аспекти, такі як управління пам'яттю, яка використовується вашою програмою, і т. д.

### Портативний

З-за своєї природи, програмного забезпечення з відкритим вихідним кодом Python був портований (тобто змінений, щоб змусити його працювати) на багатьох платформах. Всі ваші програми Python можуть працювати на будь-якій з цих платформ, не вимагаючи ніяких змін, якщо ви досить обережні, щоб уникнути будь-яких системних функцій.


Ви можете використовувати Python у Linux, Windows, FreeBSD, Mac, Solaris, ОС/2, і  Amiga, AROS, AS/400, BeOS, OS/390, z/OS, Palm OS, QNX, VMS, Psion, Acorn RISC OS, VxWorks, PlayStation, Sharp Zaurus, Windows CE і PocketPC!


Ви навіть можете використовувати платформу ,як [Kivy] (http://kivy.org) створювати ігри для вашого комп'ютера а також для iPhone, iPad і Android.

### Інтерпретований


Це вимагає невеликого пояснення.

Програма, написана на компільованій мові, як C або C++, перетворюється з вихідної мови, тобто C або C++, в мову, на якій говорить ваш комп'ютер (двійковий код, тобто 0лі і 1ці), використовуючи компілятор з різними прапорами і параметрами. При запуску програми компонувальник / завантажувач (linker/loader) копіює програму з жорсткого диска в пам'ять і запускає її.

Python, з іншого боку, не потребує компіляції в двійковому форматі. Ви просто запускаєте програму безпосередньо з вихідного коду. Всередині Python перетворює вихідний код в проміжну форму, так званий байт-кодами, а потім переводить її на рідну мову вашого комп'ютера і запускає. Все це, насправді, робить використання Python набагато простіше, так як вам не потрібно турбуватися про компіляції програми, переконуватис що відповідні бібліотеки пов'язано (linked) і завантажено і т. д. Це також робить програми на Python набагато більш портативними, так як ви можете просто скопіювати програму на інший комп'ютер і вонп просто запрацює!

### Об'єктно-Орієнтований Об'єктно-Орієнтованість

Python підтримує процедурно-орієнтоване програмування, а також об'єктно-орієнтоване програмування. У _procedure-oriented_ (процедурно-орієнтованих) мовах, програма побудована навколо процедур або функцій, які не що інше, як багаторазові частини програм. У _object-oriented_ (об'єктно-орієнтованих) мовах, програма побудована навколо об'єктів, які поєднують в собі дані і функціональність. Python має дуже потужний, але спрощений спосіб виконання ООП, особливо в порівнянні з великими мовами, такими як C++ або Java.

### Розширюваний

Якщо вам потрібен аби критичний фрагмент коду виконувався дуже швидко, або ви хочете, щоб якийсь фрагмент алгоритму не був відкритий, ви можете запграмувати цю частину своєї програми на C або C++, а потім використовувати її зі своєї програми Python.

### Вбудований (вбудоваємий)

Ви можете вбудувати Python в свої програми на C/C++, щоб дати можливості _scripting_ для користувачів вашої програми.

### велика бібліотека


Стандартна бібліотека Python дійсно величезна. Це може допомогти вам робити різні речі, пов'язані з регулярними виразами,генерацією докумнетації, тестуванням модулів, багатопоточністю, базами даних, веб-браузерами, програми з CGI, FTP, електронною поштою,XML, XML-RPC, HTML, WAV файлами, криптографією, GUI (графічний інтерфейс користувача), та інші системно залежними речима. Пам'ятайте, що все це завжди доступно скрізь, де встановлено Python. Це називається _batteries Included_ (_батарейки включено_, _Батарейки у комплекті_) філософія Python.


Крім стандартної бібліотеки, існують різні інші високоякісні бібліотеки, які ви можете знайти в [Python Package Index] (http://pypi.python.org/pypi).

### Підсумок

Python-це дійсно захоплююча і потужна мова. Вона має правильне поєднання продуктивності і функцій, які роблять написання програм на Python, таким веселим і легким.

## Python 3 проти 2 Python 3 VS 2

Ви можете ігнорувати цей розділ, якщо вас не цікавить різниця між "Python версії 2 і версії Python 3". Але, будь ласка, майте на увазі, яку версію ви використовуєте. Ця книга написана для Python версії 3.


Пам'ятайте, що як тільки ви правильно зрозуміли і навчилися використовувати одну версію, ви можете легко дізнатися відмінності і використовувати іншу. Важка частина це вивчення програмування і розуміння основ самої мови Python. Це наша мета в цій книзі, і як тільки ви досягли цієї мети, ви можете легко використовувати Python 2 і Python 3 в залежності від вашої ситуації.

Докладніше про відмінності між Python 2 і Python 3, див.:


- [Майбутнє Python 2][The future of Python 2] (http://lwn.net/Articles/547191/)
- [Перенесення коду Python 2 на Python 3] [Porting Python 2 Code to Python 3](https://docs.python.org/3/howto/pyporting.html)
-[ Написання коду, який працює під Python2 і 3][Writing code that runs under both Python2 and 3](https://wiki.python.org/moin/PortingToPy3k/BilingualQuickRef)
- [Підтримка Python 3: докладний посібник][Supporting Python 3: An in-depth guide] (http://python3porting.com)



## Що Говорять Програмісти

Можливо, Вам буде цікаво прочитати, що великі хакери, такі як ESR, говорять про Python:

 Ерік Раймонд (_Eric S. Raymond_)-автор книги "собор і базар" ("The Cathedral and the Bazaar"), а також людина, яка придумала термін "відкрите джерело"("Відкрите програмне забезпечення") (_Open Source_). Він каже ,що [Python став його улюбленою мовою програмування] (http://www.python.org/about/success/esr/). Ця стаття була справжнім натхненням для моєї першої спроби Python.

- _Bruce Eckel_ автор знаменитого 'Думай  Java" 'Thinking in Java' і " мислення в с++''Thinking in C++'. Він каже, що жодна мова не зробила його більш продуктивним, ніж Python. Він каже, що Python, мабуть, єдина мова, яка зосереджується на спрощенні програмування. Прочитайте [повне інтерв'ю] (http://www.artima.com/intv/aboutme.html) для більш детальної інформації.

- _peter Norvig_-відомий автор Lisp і директор з якості пошуку в Google (спасибі Гвідо ван Россуму за вказівку на це). Він каже, що [писати на Python-це як писати в псевдокоде](https://news.ycombinator.com/item?id=1803815). Він каже, що Python завжди був невід'ємною частиною Google. Ви можете перевірити це твердження, переглянувши сторінку [Робота Google]Google Jobs] (http://www.google.com/jobs/index.html, в якій перелічено знання Python в якості вимоги для інженерів-програмістів.

