# Роботу виконала студентка ***Шроль Софія Григорівна***
> ***Київський політехнічний інституту, ІТС, група ТЗ-22***

## Lab1

В данній лабораторній роботі я встановила *IDE* , *JDK*, а також вивела у командний рядок та термінал *IDE* фразу "***Hello World***":
java
System.out.println("Hello world");

                               Контрольні питання:
1. Чим компіляція відрізняється від інтерпретації? Які переваги кожної з них?

Компіляція та інтерпретація — це два різні способи виконання програм, написаних мовами програмування. Кожен з них має свої особливості, переваги та недоліки.
         Компіляція
Компіляція — це процес перекладу коду програми, написаного мовою програмування високого рівня, у машинний код (який може виконуватися безпосередньо процесором).
Характеристики компіляції:
1.	Переклад всієї програми: Усі інструкції програми перекладаються в машинний код за один раз перед виконанням.
2.	Отримання виконуваного файлу: Результатом є виконуваний файл (наприклад, .exe в Windows).
3.	Приклад мов: C, C++, Rust, Go.
Переваги компіляції:
•	Швидкість виконання: Після компіляції програма виконується дуже швидко, оскільки не потребує перекладу під час роботи.
•	Оптимізація: Компілятори можуть оптимізувати код для конкретного обладнання.
•	Захист коду: Вихідний код не розкривається, оскільки користувач отримує лише виконуваний файл.
Недоліки компіляції:
•	Час компіляції: Компіляція може займати значний час, особливо для великих програм.
•	Проблеми з переносимістю: Виконуваний файл залежить від платформи (архітектури процесора та операційної системи).

         Інтерпретація
Інтерпретація — це процес виконання програми безпосередньо без її попереднього перекладу в машинний код. Інтерпретатор читає вихідний код, аналізує його та виконує.
Характеристики інтерпретації:
1.	Построчно виконання: Код виконується построчно або командно.
2.	Відсутність виконуваного файлу: Код виконується "на льоту", без створення окремого виконуваного файлу.
3.	Приклад мов: Python, JavaScript, Ruby.
Переваги інтерпретації:
•	Гнучкість і простота: Легше тестувати та відлагоджувати код, оскільки зміни в коді не потребують повторної компіляції.
•	Портативність: Один і той самий код може виконуватися на різних платформах, якщо для них доступний інтерпретатор.
Недоліки інтерпретації:
•	Повільніше виконання: Кожна інструкція аналізується під час виконання, що уповільнює програму.
•	Залежність від інтерпретатора: Для виконання програми потрібен інтерпретатор, який повинен бути встановлений на кожній платформі.

Коли вибирати?
•	Компіляція підходить для великих, продуктивних систем, де важлива швидкість виконання, наприклад, ігор, операційних систем.
•	Інтерпретація ідеальна для сценаріїв швидкої розробки, скриптів і веб-додатків, де важливі простота та гнучкість.

2. Що таке початковий код, байткод, машинний код? Яка між ними різниця? Що таке JIT-компіляція?

1. Початковий код
Початковий код (source code) — це текст програми, написаний мовою програмування високого рівня (наприклад, Python, C++, Java). Він читається і редагується програмістами.
Особливості:
•	Людинозрозумілий (використовує синтаксис мови програмування).
•	Не виконується безпосередньо процесором.
•	Потребує компіляції або інтерпретації, щоб стати машинним кодом.
________________________________________
2. Байткод
Байткод (bytecode) — це проміжний код, створений після компіляції початкового коду, але до його виконання. Він не є машинним кодом і не може виконуватися процесором напряму.
Особливості:
•	Призначений для віртуальних машин (наприклад, JVM для Java або PVM для Python).
•	Платформонезалежний, оскільки може виконуватися на будь-якій системі з відповідною віртуальною машиною.
•	Оптимізує процес виконання завдяки єдиній трансляції байткоду.
Приклади:
•	У Java компіляція генерує .class файли, які містять байткод.
•	У Python байткод зберігається у файлах .pyc.
________________________________________
3. Машинний код
Машинний код (machine code) — це інструкції, які безпосередньо виконує процесор. Він написаний у двійковому форматі (послідовності 0 і 1).
Особливості:
•	Залежить від апаратного забезпечення (архітектури процесора).
•	Виконується дуже швидко.
•	Генерується компілятором або JIT-компілятором із початкового коду чи байткоду.
________________________________________
Різниця між початковим кодом, байткодом і машинним кодом:
Характеристика	Початковий код	Байткод	Машинний код
Призначення	Для розробників	Для віртуальних машин	Для процесора
Зрозумілість	Людинозрозумілий	Проміжний код	Зрозумілий лише процесору
Портативність	Висока	Висока	Низька (залежить від платформи)
Швидкість виконання	Не виконується напряму	Помірна	Найвища
________________________________________
4. JIT-компіляція
JIT-компіляція (Just-In-Time Compilation) — це метод комбінованого виконання коду, який поєднує елементи компіляції та інтерпретації.
Як працює:
1.	Початковий код перекладається в байткод (наприклад, у Java чи .NET).
2.	Байткод виконується віртуальною машиною.
3.	JIT-компілятор аналізує часто використовувані частини коду (гарячі ділянки) і перекладає їх у машинний код під час виконання.
Особливості JIT-компіляції:
•	Відбувається "на льоту" (під час виконання програми).
•	Забезпечує кращу продуктивність, ніж інтерпретація.
•	Адаптується до конкретної платформи (наприклад, може оптимізувати код під специфічний процесор).
Приклади використання:
•	Віртуальна машина Java (JVM).
•	.NET CLR.
•	Сучасні браузери для виконання JavaScript.
________________________________________
Порівняння JIT і традиційної компіляції:
Параметр	Традиційна компіляція	JIT-компіляція
Час перекладу	Перед виконанням програми	Під час виконання
Оптимізація	Загальна	Локальна (для конкретного запуску)
Швидкість запуску	Повільніше	Швидше
Продуктивність	Висока	Дуже висока (з оптимізацією)

JIT-компіляція поєднує переваги обох підходів і використовується для продуктивного виконання кросплатформених програм.

3. Що таке віртуальна машина?

Віртуальна машина (ВМ)
Віртуальна машина — це програмне або апаратне середовище, яке емулює роботу реального комп'ютера, дозволяючи виконувати програми, незалежно від їхньої платформи або операційної системи.
Особливості віртуальної машини:
1.	Ізоляція: Програми, що виконуються у ВМ, ізольовані від реальної операційної системи та інших програм.
2.	Кросплатформеність: Забезпечує виконання коду на будь-якому пристрої, де встановлена відповідна віртуальна машина.
3.	Абстракція: Ховає деталі апаратного забезпечення та операційної системи.
________________________________________
Типи віртуальних машин
1. Віртуальні машини для виконання програм
Ці машини створені для виконання байткоду, згенерованого з початкового коду, і забезпечення кросплатформеності програм.
•	Приклад:
o	JVM (Java Virtual Machine) — виконує байткод Java, незалежно від платформи.
o	Python Virtual Machine (PVM) — інтерпретує байткод Python.
o	.NET CLR (Common Language Runtime) — забезпечує виконання байткоду мов C#, VB.NET тощо.
2. Системні віртуальні машини
Ці машини емулюють роботу цілого комп’ютера, включаючи процесор, оперативну пам’ять, пристрої вводу-виводу тощо.
•	Приклад:
o	VirtualBox — дозволяє запускати іншу операційну систему (наприклад, Linux у Windows).
o	VMware — інструмент для віртуалізації серверів і робочих станцій.
o	Hyper-V (Microsoft).
________________________________________
Принцип роботи віртуальної машини
1.	Інтерпретація байткоду: ВМ виконує байткод, який є незалежним від реального обладнання.
2.	Компіляція "на льоту" (JIT): У багатьох ВМ використовується JIT-компіляція, яка перетворює байткод у машинний код під час виконання програми.
3.	Управління ресурсами: Віртуальна машина забезпечує безпечний доступ до пам’яті, потоків і файлів.
________________________________________
Переваги віртуальних машин
•	Кросплатформеність: Код можна запускати на різних платформах без змін.
•	Безпека: Ізольоване середовище захищає реальну систему від потенційно небезпечного коду.
•	Мобільність: Легко переносити віртуальні машини між різними пристроями або серверами.
________________________________________
Недоліки віртуальних машин
•	Продуктивність: Виконання віртуалізованих програм часто повільніше, ніж нативних.
•	Ресурсоємність: Для роботи ВМ потрібна достатня кількість оперативної пам’яті та обчислювальних ресурсів.
________________________________________
Застосування віртуальних машин
1.	Розробка програмного забезпечення: Написання та тестування кросплатформених додатків.
2.	Веб-додатки: Виконання серверного коду (наприклад, JVM для веб-серверів на Java).
3.	Тестування: Безпечний запуск нових операційних систем або програм.
4.	Хмарні обчислення: Забезпечення ізоляції між клієнтами віртуальних серверів.
Віртуальна машина — ключовий інструмент для створення гнучких і масштабованих програмних рішень у сучасному світі IT.

4. Що таке кросплатформність? Чи є кросплатформними застосунки на мові Java? Чи є кросплатформною віртуальна машина Java?

Кросплатформність — це властивість програмного забезпечення працювати на різних операційних системах і апаратних платформах без необхідності модифікацій або значного переписування коду.
Основні риси кросплатформності:
1.	Універсальність: Код або програма можуть виконуватись на Windows, macOS, Linux та інших платформах.
2.	Економія ресурсів: Розробникам не потрібно створювати окрему версію програми для кожної операційної системи.
3.	Зручність для користувачів: Забезпечує однакову функціональність на різних пристроях.
________________________________________
Чи є кросплатформними застосунки на мові Java?
Так, застосунки на мові Java є кросплатформними. Це досягається завдяки використанню байткоду і Java Virtual Machine (JVM).
Механізм кросплатформності Java:
1.	Код компілюється в байткод: Початковий код Java (файл .java) компілюється у байткод (файл .class), який незалежний від платформи.
2.	Байткод виконується на JVM: Віртуальна машина Java інтерпретує байткод і забезпечує його виконання на конкретній платформі.
3.	Єдина вимога: Наявність JVM на пристрої.
Таким чином, якщо JVM доступна для операційної системи (а вона доступна для більшості сучасних ОС), Java-застосунок буде працювати на цій платформі.
________________________________________
Чи є кросплатформною віртуальна машина Java?
Віртуальна машина Java (JVM) сама по собі не є кросплатформною. Вона створена для роботи на конкретній операційній системі та апаратній платформі. Наприклад, існують окремі реалізації JVM для Windows, macOS, Linux тощо.
Як JVM забезпечує кросплатформність Java-застосунків:
1.	JVM адаптується до специфіки операційної системи та апаратного забезпечення.
2.	Вона приховує ці деталі від байткоду, що виконується, створюючи однакове середовище для Java-застосунків на різних платформах.
Таким чином, хоч JVM і залежить від платформи, завдяки їй забезпечується кросплатформність Java-застосунків.
________________________________________
Переваги кросплатформності Java:
•	Широке охоплення: Java-застосунки можуть працювати на серверах, ПК, мобільних пристроях тощо.
•	Економія часу розробки: Один код для багатьох платформ.
•	Зручність для бізнесу: Спрощується підтримка та розгортання програм.
Обмеження кросплатформності Java:
•	Продуктивність: Використання JVM може додавати накладні витрати порівняно з нативними програмами.
•	Залежність від JVM: Java-застосунки працюють лише за наявності встановленої JVM.
Отже, Java — це один із найкращих виборів для створення кросплатформних програм.

5. Дати пояснення кожному зі слів у початковому коді HelloWorld:
	- class
	- public
	- static
	- void
	- String
	- System
	- out
	- println

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
1. class
•   Значення: class — це ключове слово, яке використовується для оголошення класу в Java. Клас є основним будівельним блоком об'єктно-орієнтованого програмування (ООП) у Java.
•	У цьому коді:
o	HelloWorld — ім'я класу, що містить програму.
o	Клас виступає як контейнер для методу main.
________________________________________
2. public
•	Означення: public — це модифікатор доступу, який означає, що метод або клас доступний з будь-якого іншого місця у програмі.
•	У цьому коді:
o	public перед class означає, що клас HelloWorld доступний для всіх інших класів.
o	public перед методом main дозволяє JVM викликати цей метод із будь-якого місця.
________________________________________
3. static
•	Означення: static вказує, що метод або змінна належить класу, а не конкретному об'єкту цього класу.
•	У цьому коді:
o	Метод main є статичним, тобто його можна викликати без створення об'єкта класу HelloWorld.
________________________________________
4. void
•	Означення: void вказує, що метод не повертає жодного значення.
•	У цьому коді:
o	Метод main нічого не повертає, тому використовується ключове слово void.
________________________________________
5. String
•	Означення: String — це клас у Java, який використовується для зберігання текстових даних (рядків символів).
•	У цьому коді:
o	String[] args — це параметр методу main. Він представляє масив рядків, який може бути переданий програмі як аргументи командного рядка.
________________________________________
6. System
•	Означення: System — це вбудований клас у Java, який містить корисні методи та поля для взаємодії з системними ресурсами, такими як введення, виведення та управління середовищем.
•	У цьому коді:
o	System використовується для доступу до стандартного виведення через поле out.
________________________________________
7. out
•	Означення: out — це статичне поле класу System, яке представляє стандартний потік виведення (зазвичай консоль).
•	У цьому коді:
o	System.out дозволяє виводити текст на консоль.
________________________________________
8. println
•	Означення: println — це метод класу PrintStream, який виводить текст і автоматично додає символ нового рядка (\n) наприкінці.
•	У цьому коді:
o	System.out.println("Hello, World!"); друкує текст "Hello, World!" на консоль і переходить на новий рядок.
________________________________________
Загалом:
Ці слова разом створюють програму, яка використовує базові конструкції Java для виведення тексту на консоль. Ключові слова (class, public, static, void) і класи (String, System) є невід'ємною частиною Java і забезпечують її функціональність.

6. Що буде, якщо в одному з цих слів змінити регістр літер, наприклад, замість «class» написати «CLASS»?

У мові програмування Java зміна регістру літер у ключових словах або іменах класів, методів чи змінних призводить до помилок, оскільки Java є чутливою до регістру (case-sensitive). Розглянемо, що станеться, якщо змінити регістр кожного з наведених слів:
________________________________________
1. class → CLASS
•	Результат: Помилка компіляції.
•	Причина: class є ключовим словом Java, і його написання з великої літери (CLASS) не буде розпізнане як правильне ключове слово. Компілятор виведе повідомлення про синтаксичну помилку.
________________________________________
2. public → PUBLIC
•	Результат: Помилка компіляції.
•	Причина: public — це ключове слово, і зміна регістру зробить його нерозпізнаним. Компілятор вкаже на помилку в модифікаторі доступу.
________________________________________
3. static → STATIC
•	Результат: Помилка компіляції.
•	Причина: static є ключовим словом, і його неправильне написання (з великих літер) зробить програму некомпільованою.
________________________________________
4. void → VOID
•	Результат: Помилка компіляції.
•	Причина: void є ключовим словом, яке позначає, що метод не повертає значення. Зміна його регістру спричинить помилку.
________________________________________
5. String → STRING
•	Результат: Помилка компіляції.
•	Причина: String — це ім'я класу в Java стандартної бібліотеки. У Java імена класів також чутливі до регістру. Якщо написати STRING, компілятор буде шукати клас із таким ім'ям, але його не знайде, що спричинить помилку.
________________________________________
6. System → SYSTEM
•	Результат: Помилка компіляції.
•	Причина: System — це стандартний клас Java. Якщо написати SYSTEM, компілятор буде шукати клас із таким ім'ям, але його не існує.
________________________________________
7. out → OUT
•	Результат: Помилка компіляції.
•	Причина: out — це ім'я статичного поля класу System. Поля також чутливі до регістру. Якщо написати OUT, компілятор повідомить, що такого поля немає.
________________________________________
8. println → PRINTLN
•	Результат: Помилка компіляції.
•	Причина: println — це метод класу PrintStream. Зміна регістру зробить його нерозпізнаним, і компілятор виведе повідомлення про те, що такого методу не існує.
________________________________________
Висновок:
У Java чутливість до регістру є обов'язковою вимогою. Зміна регістру будь-якого ключового слова, імені класу, методу чи змінної призведе до помилок компіляції, оскільки компілятор не зможе знайти чи розпізнати відповідний елемент програми. Для уникнення проблем необхідно дотримуватися правильного синтаксису та регістру літер.

7. Чи можна в одній системі встановити одночасно кілька різних версій Java? Якщо «ні» - пояснити чому. Якщо «так» - пояснити як, і взагалі для чого комусь таке робити?

Так, в одній системі можна встановити кілька різних версій Java одночасно. Це поширена практика, особливо в розробників, які працюють із проектами, що вимагають різних версій Java.
________________________________________
Для чого це потрібно?
1.	Сумісність із проектами:
o	Деякі програми або бібліотеки можуть залежати від специфічної версії Java (наприклад, Java 8, 11 або 17).
o	Нові версії Java можуть містити зміни, які не підтримуються старими програмами.
2.	Розробка і тестування:
o	Розробники часто тестують свої програми на декількох версіях Java, щоб переконатися в їхній сумісності.
3.	Робота зі старими проєктами:
o	Якщо проект був розроблений для певної версії Java, його може бути складно або неможливо перенести на новішу версію без змін у коді.
________________________________________
Як встановити кілька версій Java?
1.	Встановлення кількох JDK (Java Development Kit):
o	Завантажте потрібні версії JDK з офіційного сайту Oracle або AdoptOpenJDK.
o	Встановіть їх у різні директорії (наприклад, C:\Program Files\Java\jdk8 і C:\Program Files\Java\jdk17).
2.	Налаштування змінної середовища JAVA_HOME:
o	JAVA_HOME використовується для вказівки поточної версії Java.
o	Змініть значення JAVA_HOME на директорію потрібної версії Java перед запуском програми.
У Windows:
o	Відкрийте "Системні змінні" → "Змінні середовища".
o	Додайте або змініть змінну JAVA_HOME.
У Linux/macOS:
o	Додайте або змініть змінну в файлі ~/.bashrc, ~/.zshrc чи іншому конфігураційному файлі:
export JAVA_HOME=/path/to/your/jdk
export PATH=$JAVA_HOME/bin:$PATH
3.	Використання менеджерів версій Java:
o	SDKMAN! (для Linux/macOS/Windows):
Інструмент для простого встановлення, керування та перемикання між версіями JDK.
	Установка SDKMAN!:
curl -s "https://get.sdkman.io" | bash
	Установка різних версій Java:
sdk install java 8.0.292-open
sdk install java 17.0.7-open
	Перемикання версій:
sdk use java 17.0.7-open
4.	Перемикання версій у командному рядку (для Windows):
o	Використовуйте скрипт або команду для тимчасової зміни версії Java:
set JAVA_HOME=C:\Program Files\Java\jdk8
set PATH=%JAVA_HOME%\bin;%PATH%
________________________________________
Можливі складнощі:
1.	Конфлікти версій:
o	Якщо встановлені версії не належно налаштовані, система може використовувати неправильну версію Java.
2.	Сумісність інструментів:
o	Деякі інструменти (наприклад, IDE) можуть автоматично підключати одну з версій Java. Важливо переконатися, що IDE використовує потрібну версію.
________________________________________
Висновок:
Мати кілька версій Java на одній системі цілком можливо і часто необхідно для забезпечення гнучкості в розробці та тестуванні. Основний виклик — це правильне налаштування змінних середовища та інструментів для роботи з різними версіями.
