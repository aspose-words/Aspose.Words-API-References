---
title: BuildVersionInfo
linktitle: BuildVersionInfo
second_title: Aspose.Words for Java
description: Provides information about the current product name and version in Java.
type: docs
weight: 50
url: /java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Provides information about the current product name and version.

To learn more, visit the [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents] documentation article.

 **Examples:** 

Shows how to display information about your installed version of Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Methods

| Method | Description |
| --- | --- |
| [getProduct()](#getProduct) | Gets the full name of the product. |
| [getVersion()](#getVersion) | Gets the product version. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Gets the full name of the product.

 **Examples:** 

Shows how to display information about your installed version of Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - The full name of the product.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Gets the product version.

 **Remarks:** 

The product version is in the "Major.Minor.Hotfix.0" format.

 **Examples:** 

Shows how to display information about your installed version of Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - The product version.
