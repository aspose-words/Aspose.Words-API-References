---
title: License
second_title: Aspose.Words for Java API Reference
description: Provides methods to license the component.
type: docs
weight: 366
url: /java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Provides methods to license the component.

To learn more, visit the [ Licensing and Subscription ][Licensing and Subscription] documentation article.


[Licensing and Subscription]: https://docs.aspose.com/words/java/licensing/
## Constructors

| Constructor | Description |
| --- | --- |
| [License()](#License) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Licenses the component. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### License() {#License}
```
public License()
```


Initializes a new instance of this class.

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




### setLicense(InputStream stream) {#setLicense-java.io.InputStream}
```
public void setLicense(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Licenses the component.

Tries to find the license in the following locations:

1. Explicit path.

2. The folder that contains the Aspose component JAR file.

3. The folder that contains the client's calling JAR file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| licenseName | java.lang.String | Can be a full or short file name. Use an empty string to switch to evaluation mode. |

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

