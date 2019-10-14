# UNIFLOC VBA #

Анализ работы скважины и скважинного оборудования 
с использованием VBA макросов Excel.

### Описание ###

* Инженерные расчеты по добыче Унифлок VBA
* Версия 7.11

Расчетные модули разработаны для обучения студентов и специалистов методам проведения инженерных расчетов добывающих скважин. Рекомендуется применение для учебных целей. Авторы стараются избегать ошибок в расчетных модулях, но не гарантируют их отсутствия. 


Возможности на текущий момент
- Расчет физико-химических свойств пластовых флюидов по двум наборам корреляций
- Расчет многофазного потока в трубах и скважине по нескольких корреляциям (Беггс Брилл, Ансари, Унифицированная TUFFP и некоторые другие)
- Расчет многофазного потока в штуцере. Корреляция Перкинса.
- Расчет характеристик УЭЦН и база характеристик УЭЦН для некоторых типов насосов
- Расчет распределения давления в фонтанирующей скважине
- Расчет распределения давления в скважине с УЭЦН

Изменения в версии 7.11
- Добавлен автоматически генерируемый программный интерфейс API для доступа к пользовательским функциям unifloc VBA через python
- Добавлены функции расчета неустановившегося режима работы скважины после запуска с постоянным дебитом
- Описание разделено на две части - руководство пользователя и сборник упражнений

Изменения в версии 7.10
- При запуске надстройки создается закладка с кнопками на панели управления Excel. Там есть кнопки для проверки версии и исправления ссылок на надстройку при переносе ее между компами.
- Мелкие исправления в названиях функций


Изменения в версии 7.9
- Добавлены функции для расчета газлифтных клапанов
- Добавлен режим расчета распределения давления газа в трубе (без трения)
- Добавлены функции расчета параметров газлифтной скважины (расчет снизу вверх и сверху вниз)

Изменения в версии 7.8.
- Добавлены функции для работы с кривыми в интерфейсе Excel (префикс "crv_")

Изменения в версии 7.7.
- Упорядочены упражнения по использованию расчетных функций
- Изменены названия ряда пользовательских функций для удобства использования
- Функции для расчета скважин (фонтан, ЭЦН, газлифт)
- Расчет асинхронного двигателя ПЭД
- Оценка коэффициента сепарации газосепаратора 
- Исправление мелких ошибок
- Доработано описание - добавлен раздел с автоматически генерируемыми описаниями функций. Компиляция документации в LuaTex

Изменения в версии 7.6
- Добавлен учет плотности газа в затрубном пространстве при расчете скважины с УЭЦН
- Обновлена схема работы со скважинами и расчета узлового анализа. Введен интерфейсный класс IWell скважины обеспечивающий одинаковое поведение всех типов скважин и типовые расчеты узлового анализа
- Сделан единий механизм работы с расчетными кривыми для всех базовых классов. Механизм реализуется классом CCurves
- Переработаны методы инициализации скважин для устранения неоднозначностей. Отдельно задается конструкция, отдельно задается распределение температуры и метод расчета температуры скважины
- В связи с переработками поменялись названия ряда методов классов скважины, поэтому изменен номер версии.

на текущий момент версия 7.6 еще в доработке. 

Изменения в версии 7.5
- Обновлен класс CWell обеспечивающий расчет по скважине с УЭЦН. 
- Добавлен класс описывающий упрощенную систему УЭЦН CESPSystemSimple. Класс обеспечивает расчет сепарации и электрических параметров по работе УЭЦН. Встраивается в CWell и обеспечивает учет работы УЭЦН в скважине. Текущие ограничения - один тип насоса (нет конусной сборки, единая кабельная линия, сопротивление кабеля не меняется по глубине с температурой, двигатель с постоянным КПД и постоянными параметрами электрическими)
- Вернулся расчет барботажа (потока газа в неподвижной жидкости) в блок многофазных расчетов и блок скважины. Сейчас барботаж считается по корреляции Ансари при очень маленьком дебите жидкости
- Добавлены интерфейсные функции Excel для расчета скважины.
- Изменена схема именования надстройки - теперь содержит только главный номер версии. Для того чтобы проще было обновлять расчетные модули на компе в ходе разработки. 


Изменения в версии 7.3
- Дополнена модель ПЭД
- Ускорены расчеты по скважине
- Изменился вызов некоторых функций Excel 
- Систематизирован расчет скважины 


### Контакты ###

* Хабибуллин Ринат
* khabibullin.ra@gubkin.ru

