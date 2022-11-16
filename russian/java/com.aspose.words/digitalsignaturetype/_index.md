---
title: DigitalSignatureType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип цифровой подписи.
type: docs
weight: 113
url: /ru/java/com.aspose.words/digitalsignaturetype/
---

**Наследование:**
java.lang.Object
```
public class DigitalSignatureType
```

Указывает тип цифровой подписи.
## Поля

| Поле | Описание |
| --- | --- |
| [CRYPTO_API](#CRYPTO-API) | Метод подписи Crypto API, используемый в двоичных документах Microsoft Word 97-2003 .DOC. |
| [UNKNOWN](#UNKNOWN) | Указывает на ошибку, неизвестный тип цифровой подписи. |
| [XML_DSIG](#XML-DSIG) | Метод подписи XmlDsig, используемый в документах OOXML и OpenDocument. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String digitalSignatureTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int digitalSignatureType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int digitalSignatureType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CRYPTO_API {#CRYPTO-API}
```
public static int CRYPTO_API
```


Метод подписи Crypto API, используемый в двоичных документах Microsoft Word 97-2003 .DOC.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Указывает на ошибку, неизвестный тип цифровой подписи.

### XML_DSIG {#XML-DSIG}
```
public static int XML_DSIG
```


Метод подписи XmlDsig, используемый в документах OOXML и OpenDocument.

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
### fromName(String digitalSignatureTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String digitalSignatureTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| digitalSignatureTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int digitalSignatureType) {#getName-int-}
```
public static String getName(int digitalSignatureType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| digitalSignatureType | int |  |

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
### toString(int digitalSignatureType) {#toString-int-}
```
public static String toString(int digitalSignatureType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| digitalSignatureType | int |  |

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
