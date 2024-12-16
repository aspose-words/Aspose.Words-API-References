---
title: X509Certificate2Wrapper
linktitle: X509Certificate2Wrapper
second_title: Aspose.Words for Java
description: JAVA-added public wrapper around ours internal X509Certificate2 in Java.
type: docs
weight: 708
url: /java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

JAVA-added public wrapper around ours internal X509Certificate2. Needed to smoothly emulate .Net api and simplify java user code. Ideally we have to use java.security.cert.X509Certificate instead this but we still didn't manage to get private key from java X509Certificate - may be fix later.
## Constructors

| Constructor | Description |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Java certificate is used to get generic certificate info: notBefore, notAfter, etc. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| password | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Java certificate is used to get generic certificate info: notBefore, notAfter, etc.

**Returns:**
java.security.cert.X509Certificate
