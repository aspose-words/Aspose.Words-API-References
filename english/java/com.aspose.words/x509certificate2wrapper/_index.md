---
title: X509Certificate2Wrapper
linktitle: X509Certificate2Wrapper
second_title: Aspose.Words for Java
description: JAVA-added public wrapper around ours internal X509Certificate2 in Java.
type: docs
weight: 644
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Java certificate is used to get generic certificate info: notBefore, notAfter, etc. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Java certificate is used to get generic certificate info: notBefore, notAfter, etc.

**Returns:**
java.security.cert.X509Certificate
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

