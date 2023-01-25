---
title: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words for Java API Reference
description: Contains settings of the digital signature timestamp.
type: docs
weight: 457
url: /java/com.aspose.words/pdfdigitalsignaturetimestampsettings/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureTimestampSettings
```

Contains settings of the digital signature timestamp.

To learn more, visit the [ Work with Digital Signatures ][Work with Digital Signatures] documentation article.


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Constructors

| Constructor | Description |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings()](#PdfDigitalSignatureTimestampSettings) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password)](#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)](#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long) | Initializes an instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getPassword()](#getPassword) | Timestamp server password. |
| [getServerUrl()](#getServerUrl) | Timestamp server URL. |
| [getTimeout()](#getTimeout) | Time-out value in milliseconds for accessing timestamp server. |
| [getUserName()](#getUserName) | Timestamp server user name. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setPassword(String value)](#setPassword-java.lang.String) | Timestamp server password. |
| [setServerUrl(String value)](#setServerUrl-java.lang.String) | Timestamp server URL. |
| [setTimeout(long value)](#setTimeout-long) | Time-out value in milliseconds for accessing timestamp server. |
| [setUserName(String value)](#setUserName-java.lang.String) | Timestamp server user name. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### PdfDigitalSignatureTimestampSettings() {#PdfDigitalSignatureTimestampSettings}
```
public PdfDigitalSignatureTimestampSettings()
```


Initializes an instance of this class.

### PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password) {#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String}
```
public PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password)
```


Initializes an instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| serverUrl | java.lang.String | Timestamp server URL. |
| userName | java.lang.String | Timestamp server user name. |
| password | java.lang.String | Timestamp server password. |

### PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout) {#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long}
```
public PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)
```


Initializes an instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| serverUrl | java.lang.String | Timestamp server URL. |
| userName | java.lang.String | Timestamp server user name. |
| password | java.lang.String | Timestamp server password. |
| timeout | long | Time-out value in milliseconds for accessing timestamp server. |

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
### getPassword() {#getPassword}
```
public String getPassword()
```


Timestamp server password. The default value is  null .

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getServerUrl() {#getServerUrl}
```
public String getServerUrl()
```


Timestamp server URL. The default value is  null . If  null , then the digital signature will not be time-stamped.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getTimeout() {#getTimeout}
```
public long getTimeout()
```


Time-out value in milliseconds for accessing timestamp server. The default value is 100 seconds.

**Returns:**
long - The corresponding long value.
### getUserName() {#getUserName}
```
public String getUserName()
```


Timestamp server user name. The default value is  null .

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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




### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Timestamp server password. The default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setServerUrl(String value) {#setServerUrl-java.lang.String}
```
public void setServerUrl(String value)
```


Timestamp server URL. The default value is  null . If  null , then the digital signature will not be time-stamped.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTimeout(long value) {#setTimeout-long}
```
public void setTimeout(long value)
```


Time-out value in milliseconds for accessing timestamp server. The default value is 100 seconds.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | long | The corresponding long value. |

### setUserName(String value) {#setUserName-java.lang.String}
```
public void setUserName(String value)
```


Timestamp server user name. The default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

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

