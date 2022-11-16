---
title: DocumentSecurity
second_title: Справочник по API Aspose.Words для Java
description: Используется как значение свойства /.
type: docs
weight: 130
url: /ru/java/com.aspose.words/documentsecurity/
---

**Наследование:**
java.lang.Object
```
public class DocumentSecurity
```

 Используется как значение для[BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties\#getSecurity--) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties\#setSecurity-int-) имущество. Указывает уровень безопасности документа в виде числового значения.
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Свойство не указывает состояния безопасности. |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | Документ защищен паролем. |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | Документ всегда должен открываться только для чтения. |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | Документ всегда должен открываться только для чтения, за исключением аннотаций. |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | Документ должен быть открыт только для чтения, если это возможно, но этот параметр можно переопределить. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String documentSecurityName)](#fromName-java.lang.String-) |  |
| [fromNames(Set documentSecurityNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int documentSecurity)](#getName-int-) |  |
| [getNames(int documentSecurity)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int documentSecurity)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NONE {#NONE}
```
public static int NONE
```


Свойство не указывает состояния безопасности.

### PASSWORD_PROTECTED {#PASSWORD-PROTECTED}
```
public static int PASSWORD_PROTECTED
```


Документ защищен паролем. (Примечание никогда не было замечено в документе до сих пор).

### READ_ONLY_ENFORCED {#READ-ONLY-ENFORCED}
```
public static int READ_ONLY_ENFORCED
```


Документ всегда должен открываться только для чтения.

### READ_ONLY_EXCEPT_ANNOTATIONS {#READ-ONLY-EXCEPT-ANNOTATIONS}
```
public static int READ_ONLY_EXCEPT_ANNOTATIONS
```


Документ всегда должен открываться только для чтения, за исключением аннотаций.

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


Документ должен быть открыт только для чтения, если это возможно, но этот параметр можно переопределить.

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
### fromName(String documentSecurityName) {#fromName-java.lang.String-}
```
public static int fromName(String documentSecurityName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set documentSecurityNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int documentSecurity) {#getName-int-}
```
public static String getName(int documentSecurity)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSecurity | int |  |

**Возвращает:**
java.lang.String
### getNames(int documentSecurity) {#getNames-int-}
```
public static Set getNames(int documentSecurity)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSecurity | int |  |

**Возвращает:**
java.util.Set
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
### toString(int documentSecurity) {#toString-int-}
```
public static String toString(int documentSecurity)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSecurity | int |  |

**Возвращает:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

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
