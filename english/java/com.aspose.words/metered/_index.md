---
title: Metered
second_title: Aspose.Words for Java API Reference
description: Provides methods to set metered key.
type: docs
weight: 402
url: /java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

Provides methods to set metered key.

To learn more, visit the [ Licensing and Subscription ][Licensing and Subscription] documentation article.

In this example, an attempt will be made to set metered public and private key the component jar file:

```

 Metered matered = new Metered();
 matered.setMeteredKey("PublicKey", "PrivateKey");
 
```


[Licensing and Subscription]: https://docs.aspose.com/words/java/licensing/
## Constructors

| Constructor | Description |
| --- | --- |
| [Metered()](#Metered) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getConsumptionCredit()](#getConsumptionCredit) | Gets consumption credit |
| [getConsumptionQuantity()](#getConsumptionQuantity) | Gets consumption file size |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String) | Sets metered public and private key. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Metered() {#Metered}
```
public Metered()
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
### getConsumptionCredit() {#getConsumptionCredit}
```
public static BigDecimal getConsumptionCredit()
```


Gets consumption credit

**Returns:**
java.math.BigDecimal - consumption quantity
### getConsumptionQuantity() {#getConsumptionQuantity}
```
public static BigDecimal getConsumptionQuantity()
```


Gets consumption file size

**Returns:**
java.math.BigDecimal - consumption quantity
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




### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Sets metered public and private key. If you purchase metered license, when start application, this API should be called, normally, this is enough. However, if always fail to upload consumption data and exceed 24 hours, the license will be set to evaluation status, to avoid such case, you should regularly check the license status, if it is evaluation status, call this API again.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| publicKey | java.lang.String | public key |
| privateKey | java.lang.String | private key |

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

