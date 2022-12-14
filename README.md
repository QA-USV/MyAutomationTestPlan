# **ТЕСТ ПЛАН** 
# **"Тестирование функционала сайта netology.ru"**

## **Introduction**
Настоящий Тест план разработан для информирования заинтересованных лиц о подходе к автоматизации тестирования функционала веб-сайта netology.ru (далее также - "Проект").

Тест план включает в себя описание объекта, цели и объема тестирования, виды тестирования, ресурсы и время, требуемые для тестирования, а также определяет ожидаемые результаты тестирования и риски, связаные с настоящим планом.

> "Заинтересованными лицами" в целях настоящего плана признаются любые лица, обладающие правом доступа к настоящему документу, включая, но не ограничиваясь, разработчиками и тестировщиками.
---
## **1. Test Strategy**

### **1.1. In Scope**
Объем этого проекта ограничен тестированием функций, описанных ниже в настоящем разделе. 

Функция, подлежащая тестированию: навигациия по сценариям перехода к форме записи и web-сервис запись на обучение по профессии "Тестировщик ПО" сайта <http://wwww.netology.ru>.

### **Cценарии тестирования:**

**I. Сценарии перехода к форме записи на обучение по профессии "Тестировщик ПО".**

**1.1. НЕЗАРЕГИСТРИРОВАННЫЙ ПОЛЬЗОВАТЕЛЬ** имеет возможность с главной страницы сайта перейти к форме записи на обучение по следующим маршрутам навигации: 
1. "Направление обучения" -> "Программирование" -> "Тестировщик ПО" -> "Записаться"
1. "Каталог курсов" (Header) -> "Программирование" –> "Тестировщик ПО" –> "Записаться" 
1. "Каталог курсов" (Header) –> "Полный каталог" –> "Тестировщик ПО" –> "Записаться" 
1. "Выбрать курс" (в “Выберите вектор развития”) –> "Тестировщик ПО" –> "Записаться"
1. "Каталог курсов" (Footer, столбец Обучение) –> "Тестировщик ПО" –> "Записаться"
> **Oжидаемый результат:** После перехода по вышеуказанным маршрутам и нажатия кнопки "Записаться" пользователь переходит на страницу с формой записи на обучение по профессии "Тестировщик ПО".

**1.2. ЗАРЕГИСТРИРОВАННЫЙ ПОЛЬЗОВАТЕЛЬ** имеет возможность с главной страницы сайта перейти к форме записи на обучение по следующим маршрутам навигации: 
1. "Направление обучения" -> "Программирование" -> "Тестировщик ПО" -> "Записаться"
1. "Каталог курсов" (Header) -> "Программирование" –> "Тестировщик ПО" –> "Записаться" 
1. "Каталог курсов" (Header) –> "Полный каталог" –> "Тестировщик ПО" –> "Записаться" 
1. "Выбрать курс" (в “Выберите вектор развития”) –> "Тестировщик ПО" –> "Записаться"
1. "Каталог курсов" (Footer, столбец Обучение) –> "Тестировщик ПО" –> "Записаться"
> **Oжидаемый результат:** После перехода по вышеуказанным маршрутам и нажатия кнопки "Записаться" пользователь переходит на страницу с формой записи на обучение по профессии "Тестировщик ПО".

**II. Сценарии заполнения формы записии на обучене по профессии "Тестировщик ПО".**

**1.1. НЕЗАРЕГИСТРИРОВАННЫЙ ПОЛЬЗОВАТЕЛЬ**

> **Позитивные сценарии**

**Поле "Имя":**
> Валидные значения: 
1. *буквы кириллицы ИЛИ латиницы (в верхнем или нижнем регистре)* 
1. *пробел (совместно с буквами)*
1. *дефис (совместно с буквами)*
1. *буква "ё"*
1. *min. количество символов: 2*
1. *max. количество символов: 64*

**Поле "Номер телефона"**
> Bалидные значения: 
1. *арабские цифры и префикс "+"*
1. *начальное значение: префикс "+"*
1. *min.количество символов: 12, включая префикс "+"*
1. *max.количество символов: 15, включая префикс "+"*

**Поле "Электронная почта":**
> Валидные значения: 
>> Имя пользователя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *буквы кириллицы для .РФ зоны* 
1. *цифры*
1. *знаки! # $ % & ‘ * + — / =? ^ _ ` { | } ~*
1. точка за исключением первого и последнего знака, которая не может повторятся
1. *min. количество символов: 1*
1. *max. количество символов: 64*
>> Доменное имя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *цифры*
1. *точка за исключением первого и последнего знака, которая не может повторяться*
1. *дефис за исключением первого и последнего знака имени хоста и в начале или в конце компонента хоста*
1. *min. количество символов: 2*
1. *max. количество символов: 63*
> **Oжидаемый результат:** После ввода валидных значений и нажатия кнопки "Записаться" появляется окно с текстом *"Поздравляем! Вы успешно записаны на обучение. Для уточнения сроков обучения и иных данных с Вами свяжется менеджер Нетологии".*

> **Негативные сценарии**

**Поле "Имя":**
> Невалидные значения: 
1. *пустое поле*
> **Oжидаемый результат:** При незаполнении поля "Имя" под полем появляется текст предупреждения *"Обязательное поле".*
1. *цифры*
1. *буквы кириллицы И английские буквы*
1. *более одного пробела подряд*
1. *более одного дефиса подряд*
1. *дефис начальное значение*
1. *дефис конечное значение*
1. *специальные символы и знаки*
1. *количество символов менее: 2*
1. *количество символов более: 64*
> **Oжидаемый результат:** После ввода невалидных значений в поле "Имя" под полем появляется текст предупреждения *"Должно стостоять из букв".*

**Поле "Номер телефона"**
> Невалидные значения: 
1. *пустое поле*
> **Oжидаемый результат:** При незаполнении поля "Номер телефона" под полем появляется текст предупреждения *"Обязательное поле".*
1. *буквы*
1. *специальные символы и знаки*
1. *начальное значение: цифра*
1. *количество символов менее: 12, включая префикс "+"*
1. *количество символов более: 15, включая префикс "+"*
1. *пробелы*
> **Oжидаемый результат:** После ввода невалидных значений в поле "Номер телефона" под полем появляется текст предупреждения *"Должно стостоять из букв".*

**Поле "Электронная почта":**
> Валидные значения: 
>> Имя пользователя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *буквы кириллицы для .РФ зоны* 
1. *цифры*
1. *знаки! # $ % & ‘ * + — / =? ^ _ ` { | } ~*
1. точка за исключением первого и последнего знака, которая не может повторятся
1. *min. количество символов: 1*
1. *max. количество символов: 64*

>> Доменное имя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *цифры*
1. *точка за исключением первого и последнего знака, которая не может повторяться*
1. *дефис за исключением первого и последнего знака имени хоста и в начале или в конце компонента хоста*
1. *min. количество символов: 2*
1. *max. количество символов: 63*
> **Oжидаемый результат:** После ввода невалидных значений в поле "Электронная почта" под полем появляется текст предупреждения *"Неверный email".*

**1.2. ЗАРЕГИСТРИРОВАННЫЙ ПОЛЬЗОВАТЕЛЬ**

> **Позитивные сценарии**

**Поле "Имя":**
> Валидные значения: 
1. *буквы кириллицы ИЛИ латиницы (в верхнем или нижнем регистре)* 
1. *пробел (совместно с буквами)*
1. *дефис (совместно с буквами)*
1. *буква "ё"*
1. *min. количество символов: 2*
1. *max. количество символов: 64*

**Поле "Номер телефона"**
> Bалидные значения: 
1. *арабские цифры и префикс "+"*
1. *начальное значение: префикс "+"*
1. *min.количество символов: 12, включая префикс "+"*
1. *max.количество символов: 15, включая префикс "+"*

**Поле "Электронная почта":**
> Валидные значения: 
>> Имя пользователя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *буквы кириллицы для .РФ зоны* 
1. *цифры*
1. *знаки! # $ % & ‘ * + — / =? ^ _ ` { | } ~*
1. точка за исключением первого и последнего знака, которая не может повторятся
1. *min. количество символов: 1*
1. *max. количество символов: 64*
>> Доменное имя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *цифры*
1. *точка за исключением первого и последнего знака, которая не может повторяться*
1. *дефис за исключением первого и последнего знака имени хоста и в начале или в конце компонента хоста*
1. *min. количество символов: 2*
1. *max. количество символов: 63*
> **Oжидаемый результат:** После ввода валидных значений и нажатия кнопки "Записаться" появляется окно с текстом *"Поздравляем! Вы успешно записаны на обучение. Для уточнения сроков обучения и иных данных с Вами свяжется менеджер Нетологии".*

> **Негативные сценарии**

**Поле "Имя":**
> Невалидные значения: 
1. *пустое поле*
> **Oжидаемый результат:** При незаполнении поля "Имя" под полем появляется текст предупреждения *"Обязательное поле".*
1. *цифры*
1. *буквы кириллицы И английские буквы*
1. *более одного пробела подряд*
1. *более одного дефиса подряд*
1. *дефис начальное значение*
1. *дефис конечное значение*
1. *специальные символы и знаки*
1. *количество символов менее: 2*
1. *количество символов более: 64*
> **Oжидаемый результат:** После ввода невалидных значений в поле "Имя" под полем появляется текст предупреждения *"Должно стостоять из букв".*

**Поле "Номер телефона"**
> Невалидные значения: 
1. *пустое поле*
> **Oжидаемый результат:** При незаполнении поля "Номер телефона" под полем появляется текст предупреждения *"Обязательное поле".*
1. *буквы*
1. *специальные символы и знаки*
1. *начальное значение: цифра*
1. *количество символов менее: 12, включая префикс "+"*
1. *количество символов более: 15, включая префикс "+"*
1. *пробелы*
> **Oжидаемый результат:** После ввода невалидных значений в поле "Номер телефона" под полем появляется текст предупреждения *"Должно стостоять из букв".*

**Поле "Электронная почта":**
> Валидные значения: 
>> Имя пользователя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *буквы кириллицы для .РФ зоны* 
1. *цифры*
1. *знаки! # $ % & ‘ * + — / =? ^ _ ` { | } ~*
1. точка за исключением первого и последнего знака, которая не может повторятся
1. *min. количество символов: 1*
1. *max. количество символов: 64*

>> Доменное имя:
1. *латинские буквы (в верхнем или нижнем регистре)* 
1. *цифры*
1. *точка за исключением первого и последнего знака, которая не может повторяться*
1. *дефис за исключением первого и последнего знака имени хоста и в начале или в конце компонента хоста*
1. *min. количество символов: 2*
1. *max. количество символов: 63*
> **Oжидаемый результат:** После ввода невалидных значений в поле "Электронная почта" под полем появляется текст предупреждения *"Неверный email".*

---
### **1.2. Out of Scope**

В рамки настоящего Проекта не входят любые иные виды нефункционального и функционального тестирования, кроме прямо поименованых в разделе 1.1. Плана.

Тестирование функционала мобильного приложения (при его наличии) не входит в Проект. 

---
### **1.3. Test Type**

Функциональное тестирование в рамках, поименованых в разделе "1.1. In Scope" Плана.

---

## **2. Test criteria**

### **2.1 Suspension Criteria**

Критерии приостановки: при падении и более 40 % тестов, тестирование подлежит приостановке до устранения командой разработчиков причин такого падения.

---
### **2.2 Exit Criteria**

Критерии успешного завершения этапа тестирования: запуск и прохождение 100% тестов.

---

## **3. Resource Planning**

### **3.1. System Resources**

| No. | Resources | Description |
|---|---|---|
| 1 | Сервер    | Сервер с установленной SUT, базой данных |
| 2 | Компьютер | Windows 10, RAM min 2GB, Chrome Ver XXX.XX (64-bit), монитор мин. 15', клавиатура, мышь |
| 3 | Network   | LAN или Wi-Fi internet line, скорость не менее 0,5 Mb/s |
| 4 | Test tool   | IDE, Selenium, Selenide, DevTools, Allure | 

---

### **3.2. Human Resources**

| No. | Member | Tasks |
|-----|---|---|
| 1 | Тест_менеджер    | Управляет всем проектом, определяет направления проекта, обеспечивает требуемые ресурсы | 
| 2 | QA_Инженер | Определяет и описывает методы автоматизированного тестирования, исполняет тесты, ведет учет результатов, готовит отчеты о дефектах |

---

## **4. Permissions**

| No. | Permissions | Description |
|-----|---|---|
| 1 | Cоздания пользователей в базе данных | Для тестирования зарегистрированным пользователем |
| 2 | Удаление созданных при тестах пользователей |
---
## **5. Risks and Issues**

| No. | Risks | Mitigation |
|-----|---|---|
| 1 | Член команды не имеет опыта тестирования web-сайтов| Заменить члена команды |
| 2 | Член команды не имеет опыта автоматизации тестирования| Заменить члена команды |
| 3 | Тест менеджер имеет недостаточный опыт управления | Заменить члена команды |
| 4 | Неверная оценка бюджета и его превышение | Определять бюджет перед началом работы и уделить много внимания планированию проекта, постоянно отслеживать и соизмерять выполнение Проекта и исполнение бюджета | 
| 5 | Отсутствие сотрудничества в команде негативно влияет на производительность | Поощрять каждого члена команды при выполнении его задач и вдохновлять на бОльшие усилия |

---

## **6. Schedule & Estimation**

| Task                                           | Member        | Estimare effort |
|------------------------------------------------|---------------|---|
| Подготовка тест-кейсов                         | QA_Инженер    | 4 чел./ч |
| Написание автоматизированных тестов            | QA_Инженер    | 8 чел./ч |
| Исполнение автоматизированных тестов           | QA_Инженер    | 4 чел./ч |
| Подготовка отчета о тестировании, баг-репортов | QA_Инженер    | 4 чел./ч |
| Управление проектом                            | Тест_менеджер | 8 чел./ч |
| **Итого**                                      |               | **28 чел./ч** |

---
## **7. Test Deliverables**

7.1 Перед тестированием
- Тест план
- Тест-кейсы

7.2 Во время тестирования
- Журнал ошибок и журнал выполнения

7.3 После тестирования
- Отчет о тестировании
- Баг-репорты