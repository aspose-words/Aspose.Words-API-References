---
title: ControlChar
second_title: Справочник по API Aspose.Words для Java
description: Управляющие символы часто встречаются в документах.
type: docs
weight: 94
url: /ru/java/com.aspose.words/controlchar/
---

**Наследование:**
java.lang.Object
```
public class ControlChar
```

Управляющие символы часто встречаются в документах.

 Чтобы узнать больше, посетите**Working With Control Characters** документальная статья.

Предоставляет как символьные, так и строковые версии одних и тех же констант. Например: строка ControlChar.LineBreak и char ControlChar.LineBreakChar имеют одно и то же значение.
## Поля

| Поле | Описание |
| --- | --- |
| [CELL](#CELL) | Символ конца ячейки таблицы или конца строки таблицы: "\\x0007" или "\\а". |
| [CELL_CHAR](#CELL-CHAR) | Конец ячейки таблицы или символ конца строки таблицы: (char)7 или "\\а". |
| [COLUMN_BREAK](#COLUMN-BREAK) | Символ конца столбца: "\\x000e". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | Символ конца столбца: (char)14. |
| [CR](#CR) | Символ возврата каретки: "\\x000d" или "\\р". |
| [CR_LF](#CR-LF) | Возврат каретки, за которым следует символ перевода строки: "\\x000d\\x000a" или "\\р\\п". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | Это символ «о», используемый в качестве значения по умолчанию в полях формы ввода текста. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | Символ конца поля MS Word: (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | Символ-разделитель полей отделяет код поля от значения поля. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | Символ начала поля MS Word: (char)19. |
| [LF](#LF) | Символ перевода строки: "\\x000a" или "\\п". |
| [LINE_BREAK](#LINE-BREAK) | Символ разрыва строки: "\\x000b" или "\\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | Символ разрыва строки: (char)11 или "\\v". |
| [LINE_FEED](#LINE-FEED) | Символ перевода строки: "\\x000a" или "\\п". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | Символ перевода строки: (char)10 или "\\п". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Неразрывный дефис в Microsoft Word равен (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | Неразрывный пробел: "\\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | Неразрывный пробел: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Необязательный дефис в Microsoft Word — (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | Символ разрыва страницы: "\\x000c" или "\\ф". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | Символ разрыва страницы: (char)12 или "\\ф". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | Символ конца абзаца: "\\x000d" или "\\р". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | Символ конца абзаца: (char)13 или "\\р". |
| [SECTION_BREAK](#SECTION-BREAK) | Символ конца раздела: "\\x000c" или "\\ф". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | Символ конца раздела: (char)12 или "\\ф". |
| [SPACE_CHAR](#SPACE-CHAR) | Пробел: (char)32. |
| [TAB](#TAB) | Символ табуляции: "\\x0009" или "\\т". |
| [TAB_CHAR](#TAB-CHAR) | Символ табуляции: (char)9 или "\\т". |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CELL {#CELL}
```
public static String CELL
```


Символ конца ячейки таблицы или конца строки таблицы: "\\x0007" или "\\а".

### CELL_CHAR {#CELL-CHAR}
```
public static char CELL_CHAR
```


Конец ячейки таблицы или символ конца строки таблицы: (char)7 или "\\а".

### COLUMN_BREAK {#COLUMN-BREAK}
```
public static String COLUMN_BREAK
```


Символ конца столбца: "\\x000e".

### COLUMN_BREAK_CHAR {#COLUMN-BREAK-CHAR}
```
public static char COLUMN_BREAK_CHAR
```


Символ конца столбца: (char)14.

### CR {#CR}
```
public static String CR
```


Символ возврата каретки: "\\x000d" или "\ \r". То же, что и[PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK).

### CR_LF {#CR-LF}
```
public static String CR_LF
```


Возврат каретки, за которым следует символ перевода строки: "\\x000d\\x000a" или "\\р\\n". Не используется как таковой в документах Microsoft Word, но обычно используется в текстовых файлах для разрывов абзаца.

### DEFAULT_TEXT_INPUT_CHAR {#DEFAULT-TEXT-INPUT-CHAR}
```
public static char DEFAULT_TEXT_INPUT_CHAR
```


Это символ «о», используемый в качестве значения по умолчанию в полях формы ввода текста.

### FIELD_END_CHAR {#FIELD-END-CHAR}
```
public static char FIELD_END_CHAR
```


Символ конца поля MS Word: (char)21.

### FIELD_SEPARATOR_CHAR {#FIELD-SEPARATOR-CHAR}
```
public static char FIELD_SEPARATOR_CHAR
```


Символ-разделитель полей отделяет код поля от значения поля. Необязательный в некоторых полях. Значение: (знак)20.

### FIELD_START_CHAR {#FIELD-START-CHAR}
```
public static char FIELD_START_CHAR
```


Символ начала поля MS Word: (char)19.

### LF {#LF}
```
public static String LF
```


Символ перевода строки: "\\x000a" или "\ \n". То же, что и[LINE\_FEED](../../com.aspose.words/controlchar\#LINE-FEED).

### LINE_BREAK {#LINE-BREAK}
```
public static String LINE_BREAK
```


Символ разрыва строки: "\\x000b" или "\\v".

### LINE_BREAK_CHAR {#LINE-BREAK-CHAR}
```
public static char LINE_BREAK_CHAR
```


Символ разрыва строки: (char)11 или "\\v".

### LINE_FEED {#LINE-FEED}
```
public static String LINE_FEED
```


Символ перевода строки: "\\x000a" или "\ \n". То же, что и[LF](../../com.aspose.words/controlchar\#LF).

### LINE_FEED_CHAR {#LINE-FEED-CHAR}
```
public static char LINE_FEED_CHAR
```


Символ перевода строки: (char)10 или "\\п".

### NON_BREAKING_HYPHEN_CHAR {#NON-BREAKING-HYPHEN-CHAR}
```
public static char NON_BREAKING_HYPHEN_CHAR
```


Неразрывный дефис в Microsoft Word равен (char)30.

Неразрывный дефис в Microsoft Word не соответствует неразрывному дефису символа Unicode U+2011, а вместо этого представляет внутреннюю информацию, которая указывает Microsoft Word отображать дефис, а не разрывать строку.

Полезная информация: http://www.cs.tut.fi/~jkorpela/dashes.html\#разрывы строк.

### NON_BREAKING_SPACE {#NON-BREAKING-SPACE}
```
public static String NON_BREAKING_SPACE
```


Неразрывный пробел: "\\x00a0".

### NON_BREAKING_SPACE_CHAR {#NON-BREAKING-SPACE-CHAR}
```
public static char NON_BREAKING_SPACE_CHAR
```


Неразрывный пробел: (char)160.

### OPTIONAL_HYPHEN_CHAR {#OPTIONAL-HYPHEN-CHAR}
```
public static char OPTIONAL_HYPHEN_CHAR
```


Необязательный дефис в Microsoft Word — (char)31.

Необязательный дефис в Microsoft Word не соответствует мягкому дефису U+00AD символа Unicode. Вместо этого он вставляет внутреннюю информацию, которая сообщает Word о возможной точке переноса.

### PAGE_BREAK {#PAGE-BREAK}
```
public static String PAGE_BREAK
```


Символ разрыва страницы: "\\x000c" или "\ \f". Обратите внимание, что он имеет то же значение, что и[SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK).

### PAGE_BREAK_CHAR {#PAGE-BREAK-CHAR}
```
public static char PAGE_BREAK_CHAR
```


Символ разрыва страницы: (char)12 или "\\ф".

### PARAGRAPH_BREAK {#PARAGRAPH-BREAK}
```
public static String PARAGRAPH_BREAK
```


Символ конца абзаца: "\\x000d" или "\ \r". То же, что и[CR](../../com.aspose.words/controlchar\#CR)

### PARAGRAPH_BREAK_CHAR {#PARAGRAPH-BREAK-CHAR}
```
public static char PARAGRAPH_BREAK_CHAR
```


Символ конца абзаца: (char)13 или "\\р".

### SECTION_BREAK {#SECTION-BREAK}
```
public static String SECTION_BREAK
```


Символ конца раздела: "\\x000c" или "\ \f". Обратите внимание, что он имеет то же значение, что и[PAGE\_BREAK](../../com.aspose.words/controlchar\#PAGE-BREAK).

### SECTION_BREAK_CHAR {#SECTION-BREAK-CHAR}
```
public static char SECTION_BREAK_CHAR
```


Символ конца раздела: (char)12 или "\\ф".

### SPACE_CHAR {#SPACE-CHAR}
```
public static char SPACE_CHAR
```


Пробел: (char)32.

### TAB {#TAB}
```
public static String TAB
```


Символ табуляции: "\\x0009" или "\\т".

### TAB_CHAR {#TAB-CHAR}
```
public static char TAB_CHAR
```


Символ табуляции: (char)9 или "\\т".

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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
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
