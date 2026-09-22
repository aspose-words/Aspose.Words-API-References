---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words لـ Java"
description: "يوفر معلومات حول اسم المنتج الحالي وإصداره في Java."
type: docs
weight: 51
url: /ar/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

يوفر معلومات حول اسم المنتج الحالي وإصداره.

لمزيد من المعلومات، قم بزيارة مقالة الوثائق [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents].

 **Examples:** 

يظهر كيفية عرض معلومات حول الإصدار المثبت من Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getProduct()](#getProduct) | يحصل على الاسم الكامل للمنتج. |
| [getVersion()](#getVersion) | يحصل على إصدار المنتج. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


يحصل على الاسم الكامل للمنتج.

 **Examples:** 

يظهر كيفية عرض معلومات حول الإصدار المثبت من Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - الاسم الكامل للمنتج.
### getVersion() {#getVersion}
```
public static String getVersion()
```


يحصل على إصدار المنتج.

 **Remarks:** 

إصدار المنتج بتنسيق "Major.Minor.Hotfix.0".

 **Examples:** 

يظهر كيفية عرض معلومات حول الإصدار المثبت من Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - إصدار المنتج.
