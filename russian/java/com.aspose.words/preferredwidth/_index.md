---
title: PreferredWidth
second_title: Справочник по API Aspose.Words для Java
description: Представляет значение и его единицу измерения, которые используются для указания предпочтительной ширины таблицы или ячейки.
type: docs
weight: 466
url: /ru/java/com.aspose.words/preferredwidth/
---

**Наследование:**
java.lang.Object
```
public class PreferredWidth
```

Представляет значение и его единицу измерения, которые используются для указания предпочтительной ширины таблицы или ячейки.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.

Предпочтительная ширина может быть указана в процентах, количестве точек или специальном значении «нет/авто».

Экземпляры этого класса неизменяемы.
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Возвращает экземпляр, представляющий значение «предпочтительная ширина не указана». |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth-) | Определяет, равен ли указанный PreferredWidth по значению текущему PreferredWidth. |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [fromPercent(double percent)](#fromPercent-double-) | Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную в процентах. |
| [fromPoints(double points)](#fromPoints-double-) | Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную с помощью количества точек. |
| [getClass()](#getClass--) |  |
| [getType()](#getType--) | Получает единицу измерения, используемую для этого предпочтительного значения ширины. |
| [getValue()](#getValue--) | Получает предпочтительное значение ширины. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


Возвращает экземпляр, представляющий значение «предпочтительная ширина не указана».

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth-}
```
public boolean equals(PreferredWidth other)
```


Определяет, равен ли указанный PreferredWidth по значению текущему PreferredWidth.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth) |  |

**Возвращает:**
логический
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### fromPercent(double percent) {#fromPercent-double-}
```
public static PreferredWidth fromPercent(double percent)
```


Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную в процентах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| percent | double | Значение должно быть от 0 до 100. |

**Возвращает:**
[PreferredWidth](../../com.aspose.words/preferredwidth)
### fromPoints(double points) {#fromPoints-double-}
```
public static PreferredWidth fromPoints(double points)
```


Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную с помощью количества точек.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | double |  Значение должно быть от 0 до 22 дюймов (22\* 72 балла). |

**Возвращает:**
[PreferredWidth](../../com.aspose.words/preferredwidth)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getType() {#getType--}
```
public int getType()
```


Получает единицу измерения, используемую для этого предпочтительного значения ширины.

**Возвращает:**
 int - Единица измерения, используемая для этого предпочтительного значения ширины. Возвращаемое значение является одним из[PreferredWidthType](../../com.aspose.words/preferredwidthtype) константы.
### getValue() {#getValue--}
```
public double getValue()
```


Получает предпочтительное значение ширины. Единица измерения указана в[getType()](../../com.aspose.words/preferredwidth\#getType--) имущество.

**Возвращает:**
double — предпочтительное значение ширины.
### hashCode() {#hashCode--}
```
public int hashCode()
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


Возвращает удобную для пользователя строку, отображающую значение этого объекта.

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
