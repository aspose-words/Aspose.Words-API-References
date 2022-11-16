---
title: LayoutEntityType
second_title: Справочник по API Aspose.Words для Java
description: Типы объектов макета.
type: docs
weight: 359
url: /ru/java/com.aspose.words/layoutentitytype/
---

**Наследование:**
java.lang.Object
```
public class LayoutEntityType
```

Типы объектов макета.
## Поля

| Поле | Описание |
| --- | --- |
| [CELL](#CELL) | Представляет ячейку таблицы. |
| [COLUMN](#COLUMN) | Представляет столбец текста на странице. |
| [COMMENT](#COMMENT) | Представляет заполнитель для содержимого комментария. |
| [ENDNOTE](#ENDNOTE) | Представляет заполнитель для содержимого концевой сноски. |
| [FOOTNOTE](#FOOTNOTE) | Представляет заполнитель для содержимого сноски. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Представляет заполнитель для содержимого верхнего/нижнего колонтитула на странице. |
| [LINE](#LINE) | Представляет строку символов текста и встроенных объектов. |
| [NONE](#NONE) | Значение по умолчанию. |
| [NOTE](#NOTE) | Представляет заполнитель для содержимого заметки. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Представляет разделитель сносок/концевых сносок. |
| [PAGE](#PAGE) | Представляет страницу документа. |
| [ROW](#ROW) | Представляет строку таблицы. |
| [SPAN](#SPAN) | Представляет один или несколько символов в строке. |
| [TEXT_BOX](#TEXT-BOX) | Представляет текстовую область внутри фигуры. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String layoutEntityTypeName)](#fromName-java.lang.String-) |  |
| [fromNames(Set layoutEntityTypeNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int layoutEntityType)](#getName-int-) |  |
| [getNames(int layoutEntityType)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int layoutEntityType)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CELL {#CELL}
```
public static int CELL
```


 Представляет ячейку таблицы. Ячейка может иметь[LINE](../../com.aspose.words/layoutentitytype\#LINE) а также[ROW](../../com.aspose.words/layoutentitytype\#ROW) дочерние сущности.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


 Представляет столбец текста на странице. Столбец может иметь те же дочерние объекты, что и[CELL](../../com.aspose.words/layoutentitytype\#CELL) , плюс[FOOTNOTE](../../com.aspose.words/layoutentitytype\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype\#ENDNOTE) а также[NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype\#NOTE-SEPARATOR) сущности.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


 Представляет заполнитель для содержимого комментария. Комментарий может иметь[LINE](../../com.aspose.words/layoutentitytype\#LINE) а также[ROW](../../com.aspose.words/layoutentitytype\#ROW) дочерние сущности.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


 Представляет заполнитель для содержимого концевой сноски. Сноска может иметь[NOTE](../../com.aspose.words/layoutentitytype\#NOTE) дочерние сущности.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


 Представляет заполнитель для содержимого сноски. Сноска может иметь[NOTE](../../com.aspose.words/layoutentitytype\#NOTE) дочерние сущности.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


 Представляет заполнитель для содержимого верхнего/нижнего колонтитула на странице. HeaderFooter может иметь[LINE](../../com.aspose.words/layoutentitytype\#LINE) а также[ROW](../../com.aspose.words/layoutentitytype\#ROW) дочерние сущности.

### LINE {#LINE}
```
public static int LINE
```


 Представляет строку символов текста и встроенных объектов. Линия может иметь[SPAN](../../com.aspose.words/layoutentitytype\#SPAN) дочерние сущности.

### NONE {#NONE}
```
public static int NONE
```


Значение по умолчанию.

### NOTE {#NOTE}
```
public static int NOTE
```


 Представляет заполнитель для содержимого заметки. Примечание может иметь[LINE](../../com.aspose.words/layoutentitytype\#LINE) а также[ROW](../../com.aspose.words/layoutentitytype\#ROW) дочерние сущности.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


 Представляет разделитель сносок/концевых сносок. NoteSeparator может иметь[LINE](../../com.aspose.words/layoutentitytype\#LINE) а также[ROW](../../com.aspose.words/layoutentitytype\#ROW) дочерние сущности.

### PAGE {#PAGE}
```
public static int PAGE
```


 Представляет страницу документа. Страница может иметь[COLUMN](../../com.aspose.words/layoutentitytype\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype\#HEADER-FOOTER) а также[COMMENT](../../com.aspose.words/layoutentitytype\#COMMENT) дочерние сущности.

### ROW {#ROW}
```
public static int ROW
```


 Представляет строку таблицы. Ряд может иметь[CELL](../../com.aspose.words/layoutentitytype\#CELL) как дочерние сущности.

### SPAN {#SPAN}
```
public static int SPAN
```


Представляет один или несколько символов в строке. Сюда входят специальные символы, такие как маркеры начала/конца поля, закладки и комментарии. Span не может иметь дочерних объектов.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


 Представляет текстовую область внутри фигуры. Текстовое поле может иметь[LINE](../../com.aspose.words/layoutentitytype\#LINE) а также[ROW](../../com.aspose.words/layoutentitytype\#ROW) дочерние сущности.

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
### fromName(String layoutEntityTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String layoutEntityTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int layoutEntityType) {#getName-int-}
```
public static String getName(int layoutEntityType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityType | int |  |

**Возвращает:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int-}
```
public static Set getNames(int layoutEntityType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityType | int |  |

**Возвращает:**
java.util.Set
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
### toString(int layoutEntityType) {#toString-int-}
```
public static String toString(int layoutEntityType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityType | int |  |

**Возвращает:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

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
