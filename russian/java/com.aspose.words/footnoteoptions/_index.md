---
title: FootnoteOptions
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры нумерации сносок для документа или раздела.
type: docs
weight: 293
url: /ru/java/com.aspose.words/footnoteoptions/
---

**Наследование:**
java.lang.Object
```
public class FootnoteOptions
```

Представляет параметры нумерации сносок для документа или раздела.

 Чтобы узнать больше, посетите**Working with Footnote and Endnote** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColumns()](#getColumns--) | Указывает количество столбцов, в которых форматируется область сносок. |
| [getLocation()](#getLocation--) |  |
| [getNumberStyle()](#getNumberStyle--) | Указывает числовой формат для автоматически нумерованных сносок. |
| [getPosition()](#getPosition--) | Определяет положение сносок. |
| [getRestartRule()](#getRestartRule--) | Определяет, когда перезапускается автоматическая нумерация. |
| [getStartNumber()](#getStartNumber--) | Задает начальный номер или символ для первых автоматически нумерованных сносок. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColumns(int value)](#setColumns-int-) | Указывает количество столбцов, в которых форматируется область сносок. |
| [setLocation(int value)](#setLocation-int-) |  |
| [setNumberStyle(int value)](#setNumberStyle-int-) | Указывает числовой формат для автоматически нумерованных сносок. |
| [setPosition(int value)](#setPosition-int-) | Определяет положение сносок. |
| [setRestartRule(int value)](#setRestartRule-int-) | Определяет, когда перезапускается автоматическая нумерация. |
| [setStartNumber(int value)](#setStartNumber-int-) | Задает начальный номер или символ для первых автоматически нумерованных сносок. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getColumns() {#getColumns--}
```
public int getColumns()
```


Указывает количество столбцов, в которых форматируется область сносок. Если это свойство имеет значение 0, область сносок форматируется с количеством столбцов в зависимости от количества столбцов на отображаемой странице. Значение по умолчанию — 0.

**Возвращает:**
int - соответствующее значение int.
### getLocation() {#getLocation--}
```
public int getLocation()
```




**Возвращает:**
инт
### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


Указывает числовой формат для автоматически нумерованных сносок.

Не все стили номеров применимы для этого свойства. Список применимых стилей чисел см. в диалоговом окне «Вставить сноску» или «Концевую сноску» в Microsoft Word. Если вы выберете стиль номера, который неприменим, Microsoft Word вернется к значению по умолчанию.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[NumberStyle](../../com.aspose.words/numberstyle) константы.
### getPosition() {#getPosition--}
```
public int getPosition()
```


Определяет положение сносок.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[FootnotePosition](../../com.aspose.words/footnoteposition) константы.
### getRestartRule() {#getRestartRule--}
```
public int getRestartRule()
```


Определяет, когда перезапускается автоматическая нумерация.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) константы.
### getStartNumber() {#getStartNumber--}
```
public int getStartNumber()
```


Задает начальный номер или символ для первых автоматически нумерованных сносок.

Это свойство действует только тогда, когда[getRestartRule()](../../com.aspose.words/footnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions\#setRestartRule-int-) установлен на[FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Возвращает:**
int - соответствующее значение int.
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




### setColumns(int value) {#setColumns-int-}
```
public void setColumns(int value)
```


Указывает количество столбцов, в которых форматируется область сносок. Если это свойство имеет значение 0, область сносок форматируется с количеством столбцов в зависимости от количества столбцов на отображаемой странице. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setLocation(int value) {#setLocation-int-}
```
public void setLocation(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


Указывает числовой формат для автоматически нумерованных сносок.

Не все стили номеров применимы для этого свойства. Список применимых стилей чисел см. в диалоговом окне «Вставить сноску» или «Концевую сноску» в Microsoft Word. Если вы выберете стиль номера, который неприменим, Microsoft Word вернется к значению по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[NumberStyle](../../com.aspose.words/numberstyle) константы. |

### setPosition(int value) {#setPosition-int-}
```
public void setPosition(int value)
```


Определяет положение сносок.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[FootnotePosition](../../com.aspose.words/footnoteposition) константы. |

### setRestartRule(int value) {#setRestartRule-int-}
```
public void setRestartRule(int value)
```


Определяет, когда перезапускается автоматическая нумерация.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) константы. |

### setStartNumber(int value) {#setStartNumber-int-}
```
public void setStartNumber(int value)
```


Задает начальный номер или символ для первых автоматически нумерованных сносок.

Это свойство действует только тогда, когда[getRestartRule()](../../com.aspose.words/footnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions\#setRestartRule-int-) установлен на[FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

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
