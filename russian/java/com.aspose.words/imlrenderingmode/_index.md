---
title: ImlRenderingMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как рукописные объекты InkML отображаются в фиксированных форматах страниц.
type: docs
weight: 345
url: /ru/java/com.aspose.words/imlrenderingmode/
---

**Наследование:**
java.lang.Object
```
public class ImlRenderingMode
```

Указывает, как объекты рукописного ввода (InkML) отображаются в фиксированных форматах страниц.
## Поля

| Поле | Описание |
| --- | --- |
| [FALLBACK](#FALLBACK) | Если для объекта рукописного ввода (InkML) доступна резервная форма, Aspose.Words отображает резервную форму вместо InkML. |
| [INK_ML](#INK-ML) | Aspose.Words игнорирует резервную форму рукописного объекта (InkML) и отображает сам InkML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int imlRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int imlRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Если для объекта рукописного ввода (InkML) доступна резервная форма, Aspose.Words отображает резервную форму вместо InkML. Обратите внимание, что после сохранения документа в фиксированном формате страницы с резервным режимом рендеринга объекты InkML в модели документа AW навсегда заменяются их резервными аналогами. В результате при повторном сохранении того же документа всегда будут использоваться резервные фигуры, даже если для ImlRenderingMode установлено значение InkML.

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words игнорирует резервную форму рукописного объекта (InkML) и отображает сам InkML. Это режим "по умолчанию".

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
### fromName(String imlRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String imlRenderingModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int imlRenderingMode) {#getName-int-}
```
public static String getName(int imlRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imlRenderingMode | int |  |

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
### toString(int imlRenderingMode) {#toString-int-}
```
public static String toString(int imlRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imlRenderingMode | int |  |

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
