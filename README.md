# JavaScriptStyle-Guide

## h2 1. Не используйте зарезервированные слова в качестве ключей объектов. Они не будут работать в IE8.

### h3 Подробнее

  // Хорошо
var superman = {
  defaults: { clark: 'kent' },
  hidden: true
};

Плохо
var superman = {
  default: { clark: 'kent' },
  private: true
};

2. Переменные
Для именования переменных используйте существительные на английском языке(не транслит!). Имя переменной должно быть осмысленным.

Имя может состоять из букв, цифр, символов $ и _, не должно начинаться с цифры.

Хорошо
var vegetables;
Плохо
var ovoschi;
var rrfgov;

3 Горизонтальные отступы
Отступ при вложенности - 2 пробела на каждый уровень вложенности.

Хорошо
if (age < 98) {
  for (var i = 0, iMax = items.length; i < iMax; ++i) {
    // тело цикла
  }
}
Плохо
if (age < 98) {
for (var i = 0, iMax = items.length; i < iMax; ++i) {
// тело цикла
}
}

4 Пробелы
Используйте пробелы между параметрами и не используйте между именем функции и скобкой;
Хорошо
function edit(name, age) {
  // тело функции
}
Плохо
function edit (name,age) {
  // тело функции
}
При создании анонимной функции необходимо использовать пробел перед скобкой;
Хорошо
function (name, age) {
  // тело функции
}
Плохо
function(name,age) {
  // тело функции
}
Используйте пробелы вокруг операторов.
Хорошо
if (age < 100) {
  // тело цикла
}
Плохо
if (age<100) {
  // тело цикла
}

5 Точка с запятой
В конце выражения обязательна точка с запятой.

Хорошо
alert('Привет');
alert('Мир');
Плохо
alert('Привет')
alert('Мир')

6. Комментарии
Для пояснения кода используются комментарии. Комментарии не исполняются интерпретатором JavaScript.

Однострочные комментарии начинаются с двойного слэша //. За ним обязательно должен идти пробел;
Многострочные комментарии располагаются между /* и */. За символом начала комментария обязательно должен идти пробел. Символ конца комментария располагается на новой строке.
Хорошо
/* Пример комментария.
Многострочного комментария.
*/

// Пример однострочного комментария.
Плохо
/*Пример комментария.
Многострочного комментария.*/

//Пример однострочного комментария.

7 Больше не используйте var
Объявляйте все переменные с помощью const или let. По умолчанию используется const, за исключением случаев, кгда нужно переназначить переменную. Ключевое слово var не должно использоваться.

Я все еще вижу, что люди пользуются var в примерах кода на StackOverflow и других сайтах. Не могу сказать, имеет ли это для них большое значение или это просто старая привычка, от которой тяжело избавиться.

// bad
var example = 42;

// good
let example = 42;

8 Стрелочные функции предпочтительны.

Стрелочные функции придают краткость синтаксису и исправляют многие сложности, с ним связанные. Отдавайте предпочтение стрелочным функциям, а не ключевым словам, особенно для вложенных функций.

// Плохо
[1, 2, 3].map(function (x) {
  const y = x + 1;
  return x * y;
});

// Хорошо
[1, 2, 3].map((x) => {
  const y = x + 1;
  return x * y;
});

9 5. Объявляйте переменные по одной.

Объявление каждой локальной переменной объявляет только одну переменную: такие объявления, как let a = 1, b = 2; не используются.

// Плохо
let a = 1, b = 2, c = 3;

// Хорошо
let a = 1;
let b = 2;
let c = 3;

10 Пустая строка между логическими блоками.

Оставляй пустую строку между логическими блоками.

//Плохо
let firstNumber = 2;
let secondNumber = 3;
let showSum = (num1, num2) => {
  //тело функции
}

//Хорошо
let firstNumber = 2;
let secondNumber = 3;

let showSum = (num1, num2) => {
  //тело функции
}
