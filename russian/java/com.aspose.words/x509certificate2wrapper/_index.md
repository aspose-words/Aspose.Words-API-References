---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words для Java"
description: "Публичный обёртка, добавленная в JAVA, вокруг нашего внутреннего X509Certificate2 в Java."
type: docs
weight: 739
url: /ru/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

Публичный обёртка, добавленная в JAVA, вокруг нашего внутреннего X509Certificate2. Необходима для плавного эмуляции .Net API и упрощения кода Java‑пользователя. В идеале следует использовать java.security.cert.X509Certificate вместо этого, но нам всё ещё не удалось получить закрытый ключ из java X509Certificate — возможно, будет исправлено позже.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Java‑сертификат используется для получения общей информации о сертификате: notBefore, notAfter и т.д. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String |  |
| пароль | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Java‑сертификат используется для получения общей информации о сертификате: notBefore, notAfter и т.д.

**Returns:**
java.security.cert.X509Certificate
