---
title: ConditionalStyle
second_title: Справочник по API Aspose.Words для Java
description: Представляет специальное форматирование, примененное к некоторой области таблицы с назначенным стилем таблицы.
type: docs
weight: 89
url: /ru/java/com.aspose.words/conditionalstyle/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ConditionalStyle implements Cloneable
```

Представляет специальное форматирование, примененное к некоторой области таблицы с назначенным стилем таблицы.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Очищает форматирование этого условного стиля. |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getBorders()](#getBorders--) | Получает коллекцию границ ячеек по умолчанию для условного стиля. |
| [getBottomPadding()](#getBottomPadding--) | Получает количество места (в пунктах) для добавления под содержимым ячеек таблицы. |
| [getClass()](#getClass--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getFont()](#getFont--) | Получает форматирование символов условного стиля. |
| [getLeftPadding()](#getLeftPadding--) | Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячеек таблицы. |
| [getParagraphFormat()](#getParagraphFormat--) | Получает форматирование абзаца условного стиля. |
| [getRightPadding()](#getRightPadding--) | Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы. |
| [getShading()](#getShading--) | Получает[Shading](../../com.aspose.words/shading) объект, который ссылается на форматирование заливки для этого условного стиля. |
| [getTopPadding()](#getTopPadding--) | Получает количество места (в пунктах) для добавления над содержимым ячеек таблицы. |
| [getType()](#getType--) | Получает область таблицы, к которой относится этот условный стиль. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Устанавливает количество места (в пунктах) для добавления под содержимым ячеек таблицы. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Задает количество места (в пунктах), добавляемого слева от содержимого ячеек таблицы. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRightPadding(double value)](#setRightPadding-double-) | Задает количество места (в пунктах), добавляемого справа от содержимого ячеек таблицы. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setTopPadding(double value)](#setTopPadding-double-) | Устанавливает количество места (в пунктах) для добавления над содержимым ячеек таблицы. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Очищает форматирование этого условного стиля.

### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ ячеек по умолчанию для условного стиля.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Набор границ ячеек по умолчанию для условного стиля.
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Получает количество места (в пунктах) для добавления под содержимым ячеек таблицы.

**Возвращает:**
double - количество места (в пунктах), которое нужно добавить под содержимым ячеек таблицы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Возвращает:**
java.lang.Объект
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getFont() {#getFont--}
```
public Font getFont()
```


Получает форматирование символов условного стиля.

**Возвращает:**
[Font](../../com.aspose.words/font) - Форматирование символов условного стиля.
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячеек таблицы.

**Возвращает:**
double - Количество места (в пунктах) для добавления слева от содержимого ячеек таблицы.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Получает форматирование абзаца условного стиля.

**Возвращает:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - Форматирование абзаца условного стиля.
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы.

**Возвращает:**
double - Количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы.
### getShading() {#getShading--}
```
public Shading getShading()
```


Получает[Shading](../../com.aspose.words/shading) объект, который ссылается на форматирование заливки для этого условного стиля.

**Возвращает:**
[Shading](../../com.aspose.words/shading) - А[Shading](../../com.aspose.words/shading) объект, который ссылается на форматирование заливки для этого условного стиля.
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Получает количество места (в пунктах) для добавления над содержимым ячеек таблицы.

**Возвращает:**
double — количество места (в пунктах), которое нужно добавить над содержимым ячеек таблицы.
### getType() {#getType--}
```
public int getType()
```


Получает область таблицы, к которой относится этот условный стиль.

**Возвращает:**
 int - область таблицы, к которой относится этот условный стиль. Возвращаемое значение является одним из[ConditionalStyleType](../../com.aspose.words/conditionalstyletype) константы.
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




### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления под содержимым ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить под содержимым ячеек таблицы. |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Задает количество места (в пунктах), добавляемого слева от содержимого ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), добавляемого слева от содержимого ячеек таблицы. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Задает количество места (в пунктах), добавляемого справа от содержимого ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления над содержимым ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить над содержимым ячеек таблицы. |

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
