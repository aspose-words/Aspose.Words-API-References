---
title: DigitalSignature
second_title: Справочник по API Aspose.Words для Java
description: Представляет цифровую подпись на документе и результат ее проверки.
type: docs
weight: 111
url: /ru/java/com.aspose.words/digitalsignature/
---

**Наследование:**
java.lang.Object
```
public class DigitalSignature
```

Представляет цифровую подпись на документе и результат ее проверки.

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificateHolder()](#getCertificateHolder--) | Возвращает объект держателя сертификата, содержащий сертификат, который использовался для подписи документа. |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | Получает комментарий о цели подписания. |
| [getIssuerName()](#getIssuerName--) | Возвращает отличительное имя субъекта издателя сертификата. |
| [getSignTime()](#getSignTime--) | Получает время подписания документа. |
| [getSignatureType()](#getSignatureType--) | Получает тип цифровой подписи. |
| [getSubjectName()](#getSubjectName--) | Возвращает различающееся имя субъекта сертификата, который использовался для подписи документа. |
| [hashCode()](#hashCode--) |  |
| [isValid()](#isValid--) | Возвращает true, если эта цифровая подпись действительна и документ не был подделан. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |
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
### getCertificateHolder() {#getCertificateHolder--}
```
public CertificateHolder getCertificateHolder()
```


Возвращает объект держателя сертификата, содержащий сертификат, который использовался для подписи документа.

**Возвращает:**
[CertificateHolder](../../com.aspose.words/certificateholder) - Объект держателя сертификата, содержащий сертификат, использовался для подписи документа.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getComments() {#getComments--}
```
public String getComments()
```


Получает комментарий о цели подписания.

**Возвращает:**
java.lang.String — Комментарий к цели подписи.
### getIssuerName() {#getIssuerName--}
```
public String getIssuerName()
```


Возвращает отличительное имя субъекта издателя сертификата.

**Возвращает:**
java.lang.String — различающееся имя субъекта сертификата, выдавшего сертификат.
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


Получает время подписания документа.

**Возвращает:**
java.util.Date — время подписания документа.
### getSignatureType() {#getSignatureType--}
```
public int getSignatureType()
```


Получает тип цифровой подписи.

**Возвращает:**
 int — тип цифровой подписи. Возвращаемое значение является одним из[DigitalSignatureType](../../com.aspose.words/digitalsignaturetype) константы.
### getSubjectName() {#getSubjectName--}
```
public String getSubjectName()
```


Возвращает различающееся имя субъекта сертификата, который использовался для подписи документа.

**Возвращает:**
java.lang.String — различающееся имя субъекта сертификата, который использовался для подписи документа.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isValid() {#isValid--}
```
public boolean isValid()
```


Возвращает true, если эта цифровая подпись действительна и документ не был подделан.

**Возвращает:**
boolean — Истинно, если эта цифровая подпись действительна и документ не был подделан.
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
