---
title: "ShapeMarkupLanguage"
linktitle: "ShapeMarkupLanguage"
second_title: "Aspose.Words Java için"
description: "Java'da şekil için kullanılan işaretleme dilini belirtir."
type: docs
weight: 615
url: /tr/java/com.aspose.words/shapemarkuplanguage/
---

**Inheritance:**
java.lang.Object
```
public class ShapeMarkupLanguage
```

Şekil için kullanılan İşaretleme dilini belirtir.

 **Examples:** 

Kaydedilen bir belgenin uyması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we configure compatibility options to comply with Microsoft Word 2003,
 // inserting an image will define its shape using VML.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2003);
 builder.insertImage(getImageDir() + "Transparent background logo.png");

 Assert.assertEquals(ShapeMarkupLanguage.VML, ((Shape) doc.getChild(NodeType.SHAPE, 0, true)).getMarkupLanguage());

 // The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
 // If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
 // any document we save while passing this object will have to follow that standard.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT);
 saveOptions.setSaveFormat(SaveFormat.DOCX);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

 // Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.Iso29500Strict.docx");

 Assert.assertEquals(ShapeMarkupLanguage.DML, ((Shape) doc.getChild(NodeType.SHAPE, 0, true)).getMarkupLanguage());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DML](#DML) | Şekli tanımlamak için Çizim İşaretleme Dili kullanılır. |
| [VML](#VML) | Şekli tanımlamak için Vektör İşaretleme Dili kullanılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String shapeMarkupLanguageName)](#fromName-java.lang.String) |  |
| [getName(byte shapeMarkupLanguage)](#getName-byte) |  |
| [getValues()](#getValues) |  |
| [toString(byte shapeMarkupLanguage)](#toString-byte) |  |
### DML {#DML}
```
public static byte DML
```


Şekli tanımlamak için Çizim İşaretleme Dili kullanılır.

 **Remarks:** 

Bu, Office Open XML için çizim konusunda yeni standarttır ve ilk kez ECMA-376 birinci baskısında (2006) ve MS Word 2007'de ortaya çıkmıştır.

### VML {#VML}
```
public static byte VML
```


Şekli tanımlamak için Vektör İşaretleme Dili kullanılır.

 **Remarks:** 

Yalnızca eski sistemler için Office Open XML'e dahil edilmiş kullanımdan kaldırılmış bir biçim.

### length {#length}
```
public static int length
```


### fromName(String shapeMarkupLanguageName) {#fromName-java.lang.String}
```
public static byte fromName(String shapeMarkupLanguageName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeMarkupLanguageName | java.lang.String |  |

**Returns:**
byte
### getName(byte shapeMarkupLanguage) {#getName-byte}
```
public static String getName(byte shapeMarkupLanguage)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static byte[] getValues()
```




**Returns:**
byte[]
### toString(byte shapeMarkupLanguage) {#toString-byte}
```
public static String toString(byte shapeMarkupLanguage)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
