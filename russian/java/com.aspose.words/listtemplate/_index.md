---
title: ListTemplate
second_title: Справочник по API Aspose.Words для Java
description: Указывает один из предопределенных форматов списка, доступных в Microsoft Word.
type: docs
weight: 375
url: /ru/java/com.aspose.words/listtemplate/
---

**Наследование:**
java.lang.Object
```
public class ListTemplate
```

Указывает один из предопределенных форматов списка, доступных в Microsoft Word.

 Значение шаблона списка используется в качестве параметра в**M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)** метод.

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков, доступным в диалоговом окне «Маркеры и нумерация» в Microsoft Word 2003.
## Поля

| Поле | Описание |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | Пуля первого уровня представляет собой наконечник стрелы персонажа Wingding. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | Пуля первого уровня представляет собой круг. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Маркированный список по умолчанию с 9 уровнями. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | Пуля первого уровня представляет собой 4-х алмазный символ Wingding. |
| [BULLET_DISK](#BULLET-DISK) | То же, что и BulletDefault. |
| [BULLET_SQUARE](#BULLET-SQUARE) | Пуля первого уровня представляет собой квадрат. |
| [BULLET_TICK](#BULLET-TICK) | Пуля первого уровня представляет собой галочку Wingding персонажа. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | То же, что и NumberDefault. |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | Номер первого уровня "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Нумерованный список по умолчанию с 9 уровнями. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | Номер первого уровня – «а.». |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | Номер первого уровня – «а)». |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | Номер первого уровня – «i.». |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | Номер первого уровня – «А.». |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | Номер первого уровня – «И.». |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Наброски списки с различными маркерами для разных уровней. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Список структуры с уровнями, связанными со стилями заголовков. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Список структуры с уровнями, связанными со стилями заголовков. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Список структуры с уровнями, связанными со стилями заголовков. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Список структуры с уровнями, связанными со стилями заголовков. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Схематический список с уровнями пронумерован «1., 1.1., 1.1.1, ...». |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Плановый список с уровнями, пронумерованными «1), а), i), (1), (а), (i), 1., а., i.». |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String listTemplateName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int listTemplate)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int listTemplate)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


Пуля первого уровня представляет собой наконечник стрелы персонажа Wingding. Остальные уровни такие же, как в BulletDefault.

Соответствует шестому шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


Пуля первого уровня представляет собой круг. Остальные уровни такие же, как в BulletDefault.

Соответствует второму шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Маркированный список по умолчанию с 9 уровнями. Пуля первого уровня – диск, пуля второго уровня – круг, пуля третьего уровня – квадрат. Затем форматирование повторяется для остальных уровней.

Каждый уровень отступает вправо на 0,25 дюйма относительно предыдущего уровня.

Соответствует первому шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


Пуля первого уровня представляет собой 4-х алмазный символ Wingding. Остальные уровни такие же, как в BulletDefault.

Соответствует 5-му шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


То же, что и BulletDefault.

Соответствует первому шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


Пуля первого уровня представляет собой квадрат. Остальные уровни такие же, как в BulletDefault.

Соответствует третьему шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


Пуля первого уровня представляет собой галочку Wingding персонажа. Остальные уровни такие же, как в BulletDefault.

Соответствует 7-му шаблону маркированного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


То же, что и NumberDefault.

Соответствует первому шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


Номер первого уровня "1)". Остальные уровни такие же, как в NumberDefault.

Соответствует второму шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Нумерованный список по умолчанию с 9 уровнями. Арабская нумерация (1., 2., 3., ...) для первого уровня, строчная буквенная нумерация (a., b., c., ...) для второго уровня, строчная римская нумерация (i., II., III., ...) для третьего уровня. Затем форматирование повторяется для остальных уровней.

Каждый уровень отступает вправо на 0,25 дюйма относительно предыдущего уровня.

Соответствует первому шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


Номер первого уровня – «а.». Остальные уровни такие же, как в NumberDefault.

Соответствует 6-му шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


Номер первого уровня – «а)». Остальные уровни такие же, как в NumberDefault.

Соответствует 5-му шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


Номер первого уровня – «i.». Остальные уровни такие же, как в NumberDefault.

Соответствует 7-му шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


Номер первого уровня – «А.». Остальные уровни такие же, как в NumberDefault.

Соответствует 4-му шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


Номер первого уровня – «И.». Остальные уровни такие же, как в NumberDefault.

Соответствует 3-му шаблону нумерованного списка в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Наброски списки с различными маркерами для разных уровней.

Соответствует 3-му шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Список структуры с уровнями, связанными со стилями заголовков.

Соответствует 4-му шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Список структуры с уровнями, связанными со стилями заголовков.

Соответствует 7-му шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Список структуры с уровнями, связанными со стилями заголовков.

Соответствует 5-му шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Список структуры с уровнями, связанными со стилями заголовков.

Соответствует 6-му шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Схематический список с уровнями пронумерован «1., 1.1., 1.1.1, ...».

Соответствует второму шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Плановый список с уровнями, пронумерованными «1), а), i), (1), (а), (i), 1., а., i.».

Соответствует первому шаблону списка структуры в диалоговом окне «Маркеры и нумерация» в Microsoft Word.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String listTemplateName) {#fromName-java.lang.String-}
```
public static int fromName(String listTemplateName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int listTemplate) {#getName-int-}
```
public static String getName(int listTemplate)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplate | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int listTemplate) {#toString-int-}
```
public static String toString(int listTemplate)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplate | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
