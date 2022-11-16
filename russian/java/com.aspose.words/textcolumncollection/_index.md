---
title: TextColumnCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов, представляющих все столбцы текста в разделе документа.
type: docs
weight: 562
url: /ru/java/com.aspose.words/textcolumncollection/
---

**Наследование:**
java.lang.Object
```
public class TextColumnCollection
```

 Коллекция[TextColumn](../../com.aspose.words/textcolumn) объекты, представляющие все столбцы текста в разделе документа.

 Чтобы узнать больше, посетите**Working with Sections** документальная статья.

 Использовать[setCount(int)](../../com.aspose.words/textcolumncollection\#setCount-int-) установить количество текстовых столбцов.

 Чтобы все столбцы были одинаковой ширины и располагались равномерно, установите[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) к**true** и укажите расстояние между столбцами в[getSpacing()](../../com.aspose.words/textcolumncollection\#getSpacing--) / [setSpacing(double)](../../com.aspose.words/textcolumncollection\#setSpacing-double-). MS Word автоматически рассчитает ширину столбцов.

 Если у вас есть**EvenlySpaced** установлен в**false** , необходимо указать ширину и интервал для каждого столбца отдельно. Используйте индексатор для доступа к отдельным[TextColumn](../../com.aspose.words/textcolumn) объекты.

При использовании нестандартной ширины столбцов убедитесь, что сумма ширины всех столбцов и промежутков между ними равна ширине страницы за вычетом левого и правого полей страницы.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает текстовый столбец по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество столбцов в разделе документа. |
| [getEvenlySpaced()](#getEvenlySpaced--) | **True**если текстовые столбцы имеют одинаковую ширину и равномерно распределены. |
| [getLineBetween()](#getLineBetween--) |  Когда**true**, добавляет вертикальную линию между столбцами. |
| [getSpacing()](#getSpacing--) | Когда столбцы расположены равномерно, получает или задает расстояние между каждым столбцом в пунктах. |
| [getWidth()](#getWidth--) | Когда столбцы расположены равномерно, получает ширину столбцов. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCount(int newCount)](#setCount-int-) | Располагает текст в указанное количество текстовых столбцов. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean-) | **True**если текстовые столбцы имеют одинаковую ширину и равномерно распределены. |
| [setLineBetween(boolean value)](#setLineBetween-boolean-) |  Когда**true**, добавляет вертикальную линию между столбцами. |
| [setSpacing(double value)](#setSpacing-double-) | Когда столбцы расположены равномерно, получает или задает расстояние между каждым столбцом в пунктах. |
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
### get(int index) {#get-int-}
```
public TextColumn get(int index)
```


Возвращает текстовый столбец по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |

**Возвращает:**
[TextColumn](../../com.aspose.words/textcolumn) - Текстовый столбец по указанному индексу.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество столбцов в разделе документа.

**Возвращает:**
int - количество столбцов в разделе документа.
### getEvenlySpaced() {#getEvenlySpaced--}
```
public boolean getEvenlySpaced()
```


**True**если текстовые столбцы имеют одинаковую ширину и равномерно распределены.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLineBetween() {#getLineBetween--}
```
public boolean getLineBetween()
```


 Когда**true**, добавляет вертикальную линию между столбцами.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


 Когда столбцы расположены равномерно, получает или задает расстояние между каждым столбцом в пунктах. Имеет эффект только тогда, когда[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) установлен на**true**.

**Возвращает:**
double - соответствующее двойное значение.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Когда столбцы расположены равномерно, получает ширину столбцов.

 Имеет эффект только тогда, когда[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) установлен на**true**.

**Возвращает:**
double - соответствующее двойное значение.
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




### setCount(int newCount) {#setCount-int-}
```
public void setCount(int newCount)
```


Располагает текст в указанное количество текстовых столбцов.

 Когда[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) является**false** а вы увеличиваете количество столбцов, новые[TextColumn](../../com.aspose.words/textcolumn) объекты создаются с нулевой шириной и интервалом. Вам нужно установить ширину и интервал для новых столбцов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newCount | int | Количество колонок, в которые должен быть помещен текст. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean-}
```
public void setEvenlySpaced(boolean value)
```


**True**если текстовые столбцы имеют одинаковую ширину и равномерно распределены.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLineBetween(boolean value) {#setLineBetween-boolean-}
```
public void setLineBetween(boolean value)
```


 Когда**true**, добавляет вертикальную линию между столбцами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


 Когда столбцы расположены равномерно, получает или задает расстояние между каждым столбцом в пунктах. Имеет эффект только тогда, когда[getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) установлен на**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

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
