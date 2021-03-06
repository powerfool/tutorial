# Вступ до інтерфейсу командного рядка

Що, це захоплює, чи не так?! Ви напишете свій перший рядок коду просто через декілька хвилин :)

**Дозвольте нам представити вас вашому новому другові: командний рядок!**

Наступні кроки покажуть вам як користуватися чорним вікном, яким користуються усі хакери. Спочатку це може видаватися трохи жахливим, однак насправді це лише командна підказка, що очікує певних команд від вас.

## Що таке командний рядок?

Вікно, котре зазвичай називають **командним рядком** або **інтерфейсом командного рядку**, є текстовою програмою для відображення і керування файлами на вашому комп'ютері (так само як, наприклад, Windows Explorer або Finder на Mac, але без графічного інтерфейсу). Інші назви командного рядка: *cmd*, *CLI*, *prompt*, *console* або *terminal*.

## Відкриваємо інтерфейс командного рядка

Щоб почати експериментувати, нам потрібно спочатку відкрити наш інтерфейс командного рядка.

### Windows

Перейдіть до меню Пуск → Усі програми → Стандартні → Командний рядок.

### Mac OS X

Додатки → Утиліти → Термінал.

### Linux

Скоріш за все Додатки → Стандартні → Термінал, але це може залежати від вашої системної версії. Якщо тут його немає, просто загугліть :)

## Командний рядок

Має з'явитися біле або чорне вікно, що очікує на ваші команди.

Якщо ви працюєте на Mac або на Linux, ви напевно побачите `$`, на зразок:

    $
    

На Windows, це знак `>`:

    >
    

Кожній команді буде передувати цей знак і один пробіл, але ви не мусите набирати їх. Ваш комп'ютер робитиме це для вас сам :)

> Просто маленьке зауваження: у вашому випадку ви, мабуть, побачите, щось на кшталт `C:\Users\ola>` або `Olas-MacBook-Air:~ ola$` перед знаком командного рядка і це є на 100% правильним. У даному навчальному матеріалі ми лише спростимо цей момент, щоб вилучити певний мінімум.

## Ваша перша команда (ЙОЙ!)

Почнемо з чогось простенького. Наберіть команду:

    $ whoami
    

або

    > whoami
    

Далі натисніть Enter. Це наш результат:

    $ whoami
    olasitarska
    

Як бачимо, комп'ютер лише виводить ваше ім'я користувача. Файно, еге ж?:)

> Спробуйте набирати кожну команду, а не копіювати і вставляти. Таким чином ви більше запам'ятаєте!

## Основи

У кожної операційної системи є трохи відмінні набори команд для командного рядку, отже, будьте певними, що виконуєте інструкції саме для вашої операційної системи. Давайте спробуємо?

### Поточна директорія

Було б чудово знати де ми наразі знаходимось, хіба ні? Давайте подивимось. Введіть цю команду і натисніть enter:

    $ pwd
    /Users/olasitarska
    

Якщо ви працюєте на Windows:

    > cd
    C:\Users\olasitarska
    

Можливо, ви побачите щось схоже на вашій машині. По тому як ви відкрили командний рядок, то зазвичай ви починаєте зі своєї домашньої папки.

> Зауваження: 'pwd' відповідає 'print working directory' (англ. надрукувати робочу папку).

* * *

### Список файлів і папок

Отже, що ж всередині? Було б круто з'ясувати. Давайте подивимось:

    $ ls
    Applications
    Desktop
    Downloads
    Music
    ...
    

Windows:

    > dir
     Directory of C:\Users\olasitarska
    05/08/2014 07:28 PM <DIR>      Applications
    05/08/2014 07:28 PM <DIR>      Desktop
    05/08/2014 07:28 PM <DIR>      Downloads
    05/08/2014 07:28 PM <DIR>      Music
    ...
    

* * *

### Змінити поточну директорію

Можливо, тепер ми можемо перейти до нашої папки Робочий стіл?

    $ cd Desktop
    

Windows:

    > cd Desktop
    

Перевірте чи дійсно щось змінилось:

    $ pwd
    /Users/olasitarska/Desktop
    

Windows:

    > cd
    C:\Users\olasitarska\Desktop
    

Ось!

> ПРОФІ хитрощі: якщо ви наберете `cd D` і потім натиснете `tab` на клавіатурі, командний рядок автоматично заповнить решту імені, таким чином можна оперувати швидше. Якщо папок, що починаються з "D" більше однієї, натисніть кнопку `tab` двічі щоб отримати список варіантів.

* * *

### Створити директорію 

Як щодо створення папки Django Girls на вашому робочому столі? Ви можете це зробити наступним чином:

    $ mkdir djangogirls
    

Windows:

    > mkdir djangogirls
    

Ця коротка команда створить папку з іменем `djangogirls` на вашому робочому столі. Може перевірити чи є вона там, просто глянувши на свій Робочий стіл або запустивши команду `ls`/`dir`! Спробуйте :)

> ПРОФІ хитрощі: Якщо ви не хочете кожного разу набирати одну й ту ж команду, спробуйте натиснути кнопки `стрілка вгору` та `стрілка вниз` на своїй клавіатурі щоб повторити нещодавно використовувані команди.

* * *

### Вправа!

Невеличкий виклик для вас: в щойно створеній папці `djangogirls` створіть папку `test`. Використайте команди `cd` та `mkdir`.

#### Розв'язання:

    $ cd djangogirls
    $ mkdir test
    $ ls
    test
    

Windows:

    > cd djangogirls
    > mkdir test
    > dir
    05/08/2014 07:28 PM <DIR>      test
    

Вітаємо! :)

* * *

### Прибираємо

Ми не хочемо залишити безлад, то ж давайте видалимо усе, що ми до цього моменту створили.

Спочатку, нам потрібно повернутися назад до директорії Робочий стіл:

    $ cd ..
    

Windows:

    > cd ..
    

Використання `cd` із `..` змінить вашу поточну директорію на батьківську (тобто папка, що містить вашу поточну папку).

Перевірте де ми:

    $ pwd
    /Users/olasitarska/Desktop
    

Windows:

    > cd
    C:\Users\olasitarska\Desktop
    

А тепер час видалити папку `djangogirls`.

> **Увага**: Видалення файлів за допомогою `del`, `rmdir` або `rm` є безповоротнім, тобто *файли будуть видалені назавжди*! То ж, будьте конче обережними із цією командою.

    $ rm -r djangogirls
    

Windows:

    > rmdir /S djangogirls
    djangogirls, Are you sure <Y/N>? Y
    

Виконано! Щоб переконатися, що папку дійсно видалена, давайте перевіримо:

    $ ls
    

Windows:

    > dir
    

### Вихід

Це все наразі! Можна тепер спокійно закрити командний рядок. Давайте зробимо це хакерським методом, добре?:)

    $ exit
    

Windows:

    > exit
    

Круто, га?:)

## Підсумок

Тут наведено підсумок деяких корисних команд:

| Команда (Windows) | Команда (Mac OS / Linux) | Опис                     | Приклад                                           |
| ----------------- | ------------------------ | ------------------------ | ------------------------------------------------- |
| exit              | exit                     | закрити вікно            | **exit**                                          |
| cd                | cd                       | змінити директорію       | **cd test**                                       |
| dir               | ls                       | список директорій/файлів | **dir**                                           |
| copy              | cp                       | скопіювати файл          | **copy c:\test\test.txt c:\windows\test.txt** |
| move              | mv                       | перемістити файл         | **move c:\test\test.txt c:\windows\test.txt** |
| mkdir             | mkdir                    | створити нову директорію | **mkdir testdirectory**                           |
| del               | rm                       | видалити директорію/файл | **del c:\test\test.txt**                        |

Тут наведено лише невелика кількість команд, котрі можна запускати у вашому командному рядку, однак, на даний момент ми не збираємося використовувати щось більше. 

Якщо вас цікавить, [ss64.com][1] містить повний список посилань на команди для усіх операційних систем.

 [1]: http://ss64.com

## Готові?

Давайте зануримось у Python!