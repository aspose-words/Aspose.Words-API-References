---
title: HyphenationOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет настроить параметры переноса документа.
type: docs
weight: 334
url: /ru/java/com.aspose.words/hyphenationoptions/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Позволяет настроить параметры переноса документа.

 Чтобы узнать больше, посетите**Working with Hyphenation** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoHyphenation()](#getAutoHyphenation--) | Получает значение, определяющее, включена ли для документа автоматическая расстановка переносов. |
| [getClass()](#getClass--) |  |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit--) | Получает максимальное количество последовательных строк, которые могут заканчиваться дефисами. |
| [getHyphenateCaps()](#getHyphenateCaps--) | Получает значение, определяющее, переносятся ли слова, написанные заглавными буквами. |
| [getHyphenationZone()](#getHyphenationZone--) | Получает расстояние в 1/20 пункта от правого поля, в пределах которого вы не хотите переносить слова. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean-) | Устанавливает значение, определяющее, включена ли автоматическая расстановка переносов для документа. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int-) | Устанавливает максимальное количество последовательных строк, которые могут заканчиваться дефисами. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean-) | Устанавливает значение, определяющее, будут ли слова, написанные заглавными буквами, переноситься через дефис. |
| [setHyphenationZone(int value)](#setHyphenationZone-int-) | Устанавливает расстояние в 1/20 пункта от правого поля, в пределах которого вы не хотите переносить слова. |
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
### getAutoHyphenation() {#getAutoHyphenation--}
```
public boolean getAutoHyphenation()
```


 Получает значение, определяющее, включена ли для документа автоматическая расстановка переносов. Значение по умолчанию для этого свойства**false**.

**Возвращает:**
boolean — значение, определяющее, включена ли для документа автоматическая расстановка переносов.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit--}
```
public int getConsecutiveHyphenLimit()
```


Получает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства равно 0.

Если значение этого свойства равно 0, любое количество последовательных строк может заканчиваться дефисами.

Это свойство не действует при сохранении в фиксированных форматах страниц, например PDF.

**Возвращает:**
int — максимальное количество последовательных строк, которые могут заканчиваться дефисами.
### getHyphenateCaps() {#getHyphenateCaps--}
```
public boolean getHyphenateCaps()
```


 Получает значение, определяющее, переносятся ли слова, написанные заглавными буквами. Значение по умолчанию для этого свойства**true**.

**Возвращает:**
boolean — значение, определяющее, переносятся ли слова, написанные заглавными буквами.
### getHyphenationZone() {#getHyphenationZone--}
```
public int getHyphenationZone()
```


Получает расстояние в 1/20 пункта от правого поля, в пределах которого вы не хотите переносить слова. Значение по умолчанию для этого свойства — 360 (0,25 дюйма).

**Возвращает:**
int - Расстояние в 1/20 пункта от правого поля, в пределах которого вы не хотите переносить слова.
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




### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean-}
```
public void setAutoHyphenation(boolean value)
```


 Устанавливает значение, определяющее, включена ли автоматическая расстановка переносов для документа. Значение по умолчанию для этого свойства**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, включена ли для документа автоматическая расстановка переносов. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int-}
```
public void setConsecutiveHyphenLimit(int value)
```


Устанавливает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства равно 0.

Если значение этого свойства равно 0, любое количество последовательных строк может заканчиваться дефисами.

Это свойство не действует при сохранении в фиксированных форматах страниц, например PDF.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Максимальное количество последовательных строк, которые могут заканчиваться дефисами. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean-}
```
public void setHyphenateCaps(boolean value)
```


 Устанавливает значение, определяющее, будут ли слова, написанные заглавными буквами, переноситься через дефис. Значение по умолчанию для этого свойства**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, будут ли слова, написанные заглавными буквами, переноситься через дефис. |

### setHyphenationZone(int value) {#setHyphenationZone-int-}
```
public void setHyphenationZone(int value)
```


Устанавливает расстояние в 1/20 пункта от правого поля, в пределах которого вы не хотите переносить слова. Значение по умолчанию для этого свойства — 360 (0,25 дюйма).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Расстояние в 1/20 пункта от правого поля, в пределах которого вы не хотите переносить слова. |

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
