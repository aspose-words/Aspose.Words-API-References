---
title: VbaModuleType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип модели в проекте VBA.
type: docs
weight: 595
url: /ru/java/com.aspose.words/vbamoduletype/
---

**Наследование:**
java.lang.Object
```
public class VbaModuleType
```

Указывает тип модели в проекте VBA.
## Поля

| Поле | Описание |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Модуль, содержащий определение нового объекта. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Модуль VBA, который расширяет методы и свойства элемента управления ActiveX, зарегистрированного в проекте. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Тип элемента проекта VBA, указывающий модуль для встроенных макросов и программных операций доступа, связанных с документом. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Набор подпрограмм и функций. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int vbaModuleType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int vbaModuleType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Модуль, содержащий определение нового объекта. Каждый экземпляр класса создает новый объект, а процедуры, определенные в модуле, становятся свойствами и методами объекта.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Модуль VBA, который расширяет методы и свойства элемента управления ActiveX, зарегистрированного в проекте.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Тип элемента проекта VBA, указывающий модуль для встроенных макросов и программных операций доступа, связанных с документом.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Набор подпрограмм и функций.

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
### fromName(String vbaModuleTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String vbaModuleTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int vbaModuleType) {#getName-int-}
```
public static String getName(int vbaModuleType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaModuleType | int |  |

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
### toString(int vbaModuleType) {#toString-int-}
```
public static String toString(int vbaModuleType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaModuleType | int |  |

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
