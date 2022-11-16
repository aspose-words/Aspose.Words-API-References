---
title: DigitalSignatureUtil
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет методы для подписания документа.
type: docs
weight: 114
url: /ru/java/com.aspose.words/digitalsignatureutil/
---

**Наследование:**
java.lang.Object
```
public class DigitalSignatureUtil
```

Предоставляет методы для подписания документа.

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.

Поскольку цифровая подпись работает с содержимым файла, а не с объектной моделью документа, эти методы вынесены в отдельный класс.

 Поддерживаемые форматы[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) а также[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [loadSignatures(InputStream stream)](#loadSignatures-java.io.InputStream-) |  |
| [loadSignatures(String fileName)](#loadSignatures-java.lang.String-) | Загружает цифровые подписи из документа. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAllSignatures(InputStream srcStream, OutputStream dstStream)](#removeAllSignatures-java.io.InputStream-java.io.OutputStream-) |  |
| [removeAllSignatures(String srcFileName, String dstFileName)](#removeAllSignatures-java.lang.String-java.lang.String-) | Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в целевой файл. |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-) |  |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-) |  |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-) |  Подписывает исходный документ, используя данные[CertificateHolder](../../com.aspose.words/certificateholder) с цифровой подписью и записывает подписанный документ в файл назначения. |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-) |  Подписывает исходный документ, используя данные[CertificateHolder](../../com.aspose.words/certificateholder) а также[SignOptions](../../com.aspose.words/signoptions) с цифровой подписью и записывает подписанный документ в файл назначения. |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### loadSignatures(InputStream stream) {#loadSignatures-java.io.InputStream-}
```
public static DigitalSignatureCollection loadSignatures(InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Возвращает:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection)
### loadSignatures(String fileName) {#loadSignatures-java.lang.String-}
```
public static DigitalSignatureCollection loadSignatures(String fileName)
```


Загружает цифровые подписи из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Путь к документу. |

**Возвращает:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - Сбор цифровых подписей. Возвращает пустую коллекцию, если файл не подписан.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeAllSignatures(InputStream srcStream, OutputStream dstStream) {#removeAllSignatures-java.io.InputStream-java.io.OutputStream-}
```
public static void removeAllSignatures(InputStream srcStream, OutputStream dstStream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |

### removeAllSignatures(String srcFileName, String dstFileName) {#removeAllSignatures-java.lang.String-java.lang.String-}
```
public static void removeAllSignatures(String srcFileName, String dstFileName)
```


Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в целевой файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcFileName | java.lang.String |  |
| dstFileName | java.lang.String |  |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) |  |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) |  |
| signOptions | [SignOptions](../../com.aspose.words/signoptions) |  |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder)
```


 Подписывает исходный документ, используя данные[CertificateHolder](../../com.aspose.words/certificateholder) с цифровой подписью и записывает подписанный документ в файл назначения.

 Документ должен быть либо[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) или же[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcFileName | java.lang.String | Имя файла документа для подписи. |
| dstFileName | java.lang.String | Имя файла вывода подписанного документа. |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | \{[CertificateHolder](../../com.aspose.words/certificateholder) объект с сертификатом, который использовался для подписи файла. |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)
```


 Подписывает исходный документ, используя данные[CertificateHolder](../../com.aspose.words/certificateholder) а также[SignOptions](../../com.aspose.words/signoptions) с цифровой подписью и записывает подписанный документ в файл назначения.

 Документ должен быть либо[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) или же[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcFileName | java.lang.String | Имя файла документа для подписи. |
| dstFileName | java.lang.String | Имя файла вывода подписанного документа. |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | \{[CertificateHolder](../../com.aspose.words/certificateholder) объект с сертификатом, который использовался для подписи файла. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions) | \{[SignOptions](../../com.aspose.words/signoptions) объект с различными вариантами подписи. |

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
