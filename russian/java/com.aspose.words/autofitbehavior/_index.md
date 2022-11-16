---
title: AutoFitBehavior
second_title: Справочник по API Aspose.Words для Java
description: Определяет, как Aspose.Words изменяет размер таблицы при вызове метода MAspose.Words.Tables.Table.AutoFitAspose.Words.Tables.AutoFitBehavior.
type: docs
weight: 15
url: /ru/java/com.aspose.words/autofitbehavior/
---

**Наследование:**
java.lang.Object
```
public class AutoFitBehavior
```

 Определяет, как Aspose.Words изменяет размер таблицы при вызове**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)** метод.
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO_FIT_TO_CONTENTS](#AUTO-FIT-TO-CONTENTS) | Aspose.Words включает опцию AutoFit, удаляет предпочтительную ширину из таблицы и всех ячеек, а затем обновляет макет таблицы. |
| [AUTO_FIT_TO_WINDOW](#AUTO-FIT-TO-WINDOW) | Когда вы используете это значение, Aspose.Words включает параметр AutoFit, устанавливает предпочтительную ширину таблицы на 100%, удаляет предпочтительную ширину из всех ячеек, а затем обновляет макет таблицы. |
| [FIXED_COLUMN_WIDTHS](#FIXED-COLUMN-WIDTHS) | Aspose.Words отключает параметр AutoFit и удаляет предпочтительный вариант with из таблицы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String autoFitBehaviorName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int autoFitBehavior)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int autoFitBehavior)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO_FIT_TO_CONTENTS {#AUTO-FIT-TO-CONTENTS}
```
public static int AUTO_FIT_TO_CONTENTS
```


Aspose.Words включает опцию AutoFit, удаляет предпочтительную ширину из таблицы и всех ячеек, а затем обновляет макет таблицы.

В результирующей таблице ширина ячеек обновляется, чтобы соответствовать содержимому таблицы. Скорее всего, таблица уменьшится.

### AUTO_FIT_TO_WINDOW {#AUTO-FIT-TO-WINDOW}
```
public static int AUTO_FIT_TO_WINDOW
```


Когда вы используете это значение, Aspose.Words включает параметр AutoFit, устанавливает предпочтительную ширину таблицы на 100%, удаляет предпочтительную ширину из всех ячеек, а затем обновляет макет таблицы.

В результате таблица занимает всю доступную ширину, а ширина ячеек обновляется в соответствии с содержимым таблицы.

### FIXED_COLUMN_WIDTHS {#FIXED-COLUMN-WIDTHS}
```
public static int FIXED_COLUMN_WIDTHS
```


Aspose.Words отключает параметр AutoFit и удаляет предпочтительный вариант with из таблицы.

 Ширина ячеек остается такой, какой она указана в их[CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-) характеристики.

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
### fromName(String autoFitBehaviorName) {#fromName-java.lang.String-}
```
public static int fromName(String autoFitBehaviorName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| autoFitBehaviorName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int autoFitBehavior) {#getName-int-}
```
public static String getName(int autoFitBehavior)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| autoFitBehavior | int |  |

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
### toString(int autoFitBehavior) {#toString-int-}
```
public static String toString(int autoFitBehavior)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| autoFitBehavior | int |  |

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
