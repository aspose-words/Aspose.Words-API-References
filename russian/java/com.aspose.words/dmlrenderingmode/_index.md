---
title: DmlRenderingMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как фигуры DrawingML отображаются в фиксированных форматах страниц.
type: docs
weight: 118
url: /ru/java/com.aspose.words/dmlrenderingmode/
---

**Наследование:**
java.lang.Object
```
public class DmlRenderingMode
```

Указывает, как фигуры DrawingML отображаются в фиксированных форматах страниц.
## Поля

| Поле | Описание |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words игнорирует резервную форму DrawingML и отображает сам DrawingML. |
| [FALLBACK](#FALLBACK) | Если для DrawingML доступна резервная форма, Aspose.Words отображает резервную форму вместо DrawingML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int dmlRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int dmlRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words игнорирует резервную форму DrawingML и отображает сам DrawingML. Это режим "по умолчанию".

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Если для DrawingML доступна резервная форма, Aspose.Words отображает резервную форму вместо DrawingML. Обратите внимание, что после сохранения документа в фиксированном формате страницы с резервным режимом рендеринга DML формы DML в модели документа AW навсегда заменяются их резервными аналогами. В результате при повторном сохранении того же документа всегда будут использоваться резервные фигуры, даже если для параметра DmlRenderingMode установлено значение DrawingML.

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
### fromName(String dmlRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String dmlRenderingModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int dmlRenderingMode) {#getName-int-}
```
public static String getName(int dmlRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlRenderingMode | int |  |

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
### toString(int dmlRenderingMode) {#toString-int-}
```
public static String toString(int dmlRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlRenderingMode | int |  |

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
