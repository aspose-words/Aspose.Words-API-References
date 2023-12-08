---
title: ShapeMarkupLanguage
linktitle: ShapeMarkupLanguage
second_title: Aspose.Words for Java
description: Specifies Markup language used for the shape in Java.
type: docs
weight: 546
url: /java/com.aspose.words/shapemarkuplanguage/
---

**Inheritance:**
java.lang.Object
```
public class ShapeMarkupLanguage
```

Specifies Markup language used for the shape.

 **Examples:** 

Shows how to set an OOXML compliance specification for a saved document to adhere to.

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
## Fields

| Field | Description |
| --- | --- |
| [DML](#DML) | Drawing Markup Language is used to define the shape. |
| [VML](#VML) | Vector Markup Language is used to define the shape. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String shapeMarkupLanguageName)](#fromName-java.lang.String) |  |
| [getName(byte shapeMarkupLanguage)](#getName-byte) |  |
| [getValues()](#getValues) |  |
| [toString(byte shapeMarkupLanguage)](#toString-byte) |  |
### DML {#DML}
```
public static byte DML
```


Drawing Markup Language is used to define the shape.

 **Remarks:** 

This is the new standard for drawing for Office Open XML which has appeared first in ECMA-376 1st edition (2006), first appeared in MS Word 2007.

### VML {#VML}
```
public static byte VML
```


Vector Markup Language is used to define the shape.

 **Remarks:** 

A deprecated format included in Office Open XML for legacy reasons only.

### length {#length}
```
public static int length
```


### fromName(String shapeMarkupLanguageName) {#fromName-java.lang.String}
```
public static byte fromName(String shapeMarkupLanguageName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeMarkupLanguageName | java.lang.String |  |

**Returns:**
byte
### getName(byte shapeMarkupLanguage) {#getName-byte}
```
public static String getName(byte shapeMarkupLanguage)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
