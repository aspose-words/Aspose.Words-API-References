---
title: CertificateHolder
second_title: Справочник по API Aspose.Words для Java
description: Представляет владельца экземпляра X509Certificate2.
type: docs
weight: 53
url: /ru/java/com.aspose.words/certificateholder/
---

**Наследование:**
java.lang.Object
```
public class CertificateHolder
```

 Представляет собой держателя**X509Certificate2** пример.

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.

**CertificateHolder** могут быть созданы только статическими фабричными методами. Он содержит экземпляр**X509Certificate2** который используется для введения в систему закрытых, открытых ключей и цепочек сертификатов. Этот класс применяется в[DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil) а также[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) вместо устаревших методов с**X509Certificate2** как параметры.
## Методы

| Метод | Описание |
| --- | --- |
| [create(byte[] certBytes, String password)](#create-byte---java.lang.String-) | Создает объект CertificateHolder, используя массив байтов хранилища PKCS12 и его пароль. |
| [create(String fileName, String password)](#create-java.lang.String-java.lang.String-) | Создает объект CertificateHolder, используя путь к хранилищу PKCS12 и его пароль. |
| [create(String fileName, String password, String alias)](#create-java.lang.String-java.lang.String-java.lang.String-) | Создает объект CertificateHolder, используя путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будут найдены закрытый ключ и сертификат. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificate()](#getCertificate--) |  Возвращает экземпляр**X509Certificate2Wrapper** который держит**X509Certificate2** который содержит закрытые, открытые ключи и цепочку сертификатов. |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### create(byte[] certBytes, String password) {#create-byte---java.lang.String-}
```
public static CertificateHolder create(byte[] certBytes, String password)
```


Создает объект CertificateHolder, используя массив байтов хранилища PKCS12 и его пароль.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| certBytes | byte[] | Массив байтов, содержащий данные из сертификата X.509. |
| password | java.lang.String | Пароль, необходимый для доступа к данным сертификата X.509. |

**Возвращает:**
[CertificateHolder](../../com.aspose.words/certificateholder) - Экземпляр CertificateHolder**T:Org.BouncyCastle.Security.InvalidParameterException** Брошен, если**certBytes** нулевой**T:Org.BouncyCastle.Security.InvalidParameterException** Брошен, если**password** нулевой
### create(String fileName, String password) {#create-java.lang.String-java.lang.String-}
```
public static CertificateHolder create(String fileName, String password)
```


Создает объект CertificateHolder, используя путь к хранилищу PKCS12 и его пароль.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла сертификата. |
| password | java.lang.String | Пароль, необходимый для доступа к данным сертификата X.509. |

**Возвращает:**
[CertificateHolder](../../com.aspose.words/certificateholder) - Экземпляр CertificateHolder**T:Org.BouncyCastle.Security.InvalidParameterException** Брошен, если**fileName** нулевой**T:Org.BouncyCastle.Security.InvalidParameterException** Брошен, если**password** нулевой
### create(String fileName, String password, String alias) {#create-java.lang.String-java.lang.String-java.lang.String-}
```
public static CertificateHolder create(String fileName, String password, String alias)
```


Создает объект CertificateHolder, используя путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будут найдены закрытый ключ и сертификат.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла сертификата. |
| password | java.lang.String | Пароль, необходимый для доступа к данным сертификата X.509. |
| alias | java.lang.String | Связанный псевдоним для сертификата и его закрытый ключ |

**Возвращает:**
[CertificateHolder](../../com.aspose.words/certificateholder) - Экземпляр CertificateHolder**T:Org.BouncyCastle.Security.InvalidParameterException** Брошен, если**fileName** нулевой**T:Org.BouncyCastle.Security.InvalidParameterException** Брошен, если**password** нулевой
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
### getCertificate() {#getCertificate--}
```
public X509Certificate2Wrapper getCertificate()
```


 Возвращает экземпляр**X509Certificate2Wrapper** который держит**X509Certificate2** который содержит закрытые, открытые ключи и цепочку сертификатов.

**Возвращает:**
[X509Certificate2Wrapper](../../com.aspose.words/x509certificate2wrapper) - пример
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
