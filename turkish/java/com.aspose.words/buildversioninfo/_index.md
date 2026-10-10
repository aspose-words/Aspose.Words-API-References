---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words Java için"
description: "Java'da geçerli ürün adı ve sürümü hakkında bilgi sağlar."
type: docs
weight: 51
url: /tr/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Mevcut ürün adı ve sürümü hakkında bilgi sağlar.

Daha fazla bilgi edinmek için, [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Aspose.Words'ün yüklü sürümü hakkında bilgiyi nasıl görüntüleyeceğinizi gösterir.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getProduct()](#getProduct) | Ürünün tam adını alır. |
| [getVersion()](#getVersion) | Ürün sürümünü alır. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Ürünün tam adını alır.

 **Examples:** 

Aspose.Words'ün yüklü sürümü hakkında bilgiyi nasıl görüntüleyeceğinizi gösterir.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Ürünün tam adı.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Ürün sürümünü alır.

 **Remarks:** 

Ürün sürümü "Major.Minor.Hotfix.0" biçimindedir.

 **Examples:** 

Aspose.Words'ün yüklü sürümü hakkında bilgiyi nasıl görüntüleyeceğinizi gösterir.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Ürün sürümü.
