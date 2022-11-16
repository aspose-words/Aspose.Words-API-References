---
title: EndnoteOptions
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры нумерации концевых сносок для документа или раздела.
type: docs
weight: 146
url: /ru/java/com.aspose.words/endnoteoptions/
---

**Наследование:**
java.lang.Object
```
public class EndnoteOptions
```

Представляет параметры нумерации концевых сносок для документа или раздела.

 Чтобы узнать больше, посетите**Working with Footnote and Endnote** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getLocation()](#getLocation--) |  |
| [getNumberStyle()](#getNumberStyle--) | Указывает числовой формат для автоматически нумерованных концевых сносок. |
| [getPosition()](#getPosition--) | Определяет положение концевых сносок. |
| [getRestartRule()](#getRestartRule--) | Определяет, когда перезапускается автоматическая нумерация. |
| [getStartNumber()](#getStartNumber--) | Указывает начальный номер или символ для первых автоматически нумерованных концевых сносок. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setLocation(int value)](#setLocation-int-) |  |
| [setNumberStyle(int value)](#setNumberStyle-int-) | Указывает числовой формат для автоматически нумерованных концевых сносок. |
| [setPosition(int value)](#setPosition-int-) | Определяет положение концевых сносок. |
| [setRestartRule(int value)](#setRestartRule-int-) | Определяет, когда перезапускается автоматическая нумерация. |
| [setStartNumber(int value)](#setStartNumber-int-) | Указывает начальный номер или символ для первых автоматически нумерованных концевых сносок. |
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


Указывает числовой формат для автоматически нумерованных концевых сносок.

Не все стили номеров применимы для этого свойства. Список применимых стилей чисел см. в диалоговом окне «Вставить сноску» или «Концевую сноску» в Microsoft Word. Если вы выберете стиль номера, который неприменим, Microsoft Word вернется к значению по умолчанию.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[NumberStyle](../../com.aspose.words/numberstyle) константы.
### getPosition() {#getPosition--}
```
public int getPosition()
```


Определяет положение концевых сносок.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[EndnotePosition](../../com.aspose.words/endnoteposition) константы.
### getRestartRule() {#getRestartRule--}
```
public int getRestartRule()
```


Определяет, когда перезапускается автоматическая нумерация.

 Не все значения применимы к концевым сноскам. Чтобы узнать, какие значения применимы, см.[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) константы.
### getStartNumber() {#getStartNumber--}
```
public int getStartNumber()
```


Указывает начальный номер или символ для первых автоматически нумерованных концевых сносок.

Это свойство действует только тогда, когда[getRestartRule()](../../com.aspose.words/endnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions\#setRestartRule-int-) установлен на[FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

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


Указывает числовой формат для автоматически нумерованных концевых сносок.

Не все стили номеров применимы для этого свойства. Список применимых стилей чисел см. в диалоговом окне «Вставить сноску» или «Концевую сноску» в Microsoft Word. Если вы выберете стиль номера, который неприменим, Microsoft Word вернется к значению по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[NumberStyle](../../com.aspose.words/numberstyle) константы. |

### setPosition(int value) {#setPosition-int-}
```
public void setPosition(int value)
```


Определяет положение концевых сносок.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[EndnotePosition](../../com.aspose.words/endnoteposition) константы. |

### setRestartRule(int value) {#setRestartRule-int-}
```
public void setRestartRule(int value)
```


Определяет, когда перезапускается автоматическая нумерация.

 Не все значения применимы к концевым сноскам. Чтобы узнать, какие значения применимы, см.[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) константы. |

### setStartNumber(int value) {#setStartNumber-int-}
```
public void setStartNumber(int value)
```


Указывает начальный номер или символ для первых автоматически нумерованных концевых сносок.

Это свойство действует только тогда, когда[getRestartRule()](../../com.aspose.words/endnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions\#setRestartRule-int-) установлен на[FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

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
