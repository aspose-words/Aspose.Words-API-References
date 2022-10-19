---
title: Metered
second_title: Aspose.Words for Java API Reference
description: Provides methods to set metered key.
type: docs
weight: 398
url: /java/com.aspose.words/metered/
---

**Inheritance:**
java.lang.Object
```
public class Metered
```

Provides methods to set metered key.

To learn more, visit the **Licensing and Subscription** documentation article.

In this example, an attempt will be made to set metered public and private key the component jar file:

```

 Metered matered = new Metered();
 matered.setMeteredKey("PublicKey", "PrivateKey");
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [Metered()](#Metered--) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String-) | Sets metered public and private key. |
| [getConsumptionQuantity()](#getConsumptionQuantity--) | Gets consumption file size |
| [getConsumptionCredit()](#getConsumptionCredit--) | Gets consumption credit |
### Metered() {#Metered--}
```
public Metered()
```


Initializes a new instance of this class.

### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String-}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Sets metered public and private key. If you purchase metered license, when start application, this API should be called, normally, this is enough. However, if always fail to upload consumption data and exceed 24 hours, the license will be set to evaluation status, to avoid such case, you should regularly check the license status, if it is evaluation status, call this API again.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| publicKey | java.lang.String | public key |
| privateKey | java.lang.String | private key |

### getConsumptionQuantity() {#getConsumptionQuantity--}
```
public static BigDecimal getConsumptionQuantity()
```


Gets consumption file size

**Returns:**
java.math.BigDecimal - consumption quantity
### getConsumptionCredit() {#getConsumptionCredit--}
```
public static BigDecimal getConsumptionCredit()
```


Gets consumption credit

**Returns:**
java.math.BigDecimal - consumption quantity
