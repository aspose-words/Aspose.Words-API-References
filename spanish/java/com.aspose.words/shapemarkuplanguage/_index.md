---
title: "ShapeMarkupLanguage"
linktitle: "ShapeMarkupLanguage"
second_title: "Aspose.Words para Java"
description: "Especifica el lenguaje de marcado usado para la forma en Java."
type: docs
weight: 615
url: /es/java/com.aspose.words/shapemarkuplanguage/
---

**Inheritance:**
java.lang.Object
```
public class ShapeMarkupLanguage
```

Especifica el lenguaje de marcado usado para la forma.

 **Examples:** 

Mostrar cómo establecer una especificación de cumplimiento OOXML para que un documento guardado la cumpla.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DML](#DML) | El Lenguaje de Marcado de Dibujo se usa para definir la forma. |
| [VML](#VML) | El Lenguaje de Marcado Vectorial se usa para definir la forma. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String shapeMarkupLanguageName)](#fromName-java.lang.String) |  |
| [getName(byte shapeMarkupLanguage)](#getName-byte) |  |
| [getValues()](#getValues) |  |
| [toString(byte shapeMarkupLanguage)](#toString-byte) |  |
### DML {#DML}
```
public static byte DML
```


El Lenguaje de Marcado de Dibujo se usa para definir la forma.

 **Remarks:** 

Este es el nuevo estándar de dibujo para Office Open XML que apareció por primera vez en la edición 1 de ECMA-376 (2006), y apareció por primera vez en MS Word 2007.

### VML {#VML}
```
public static byte VML
```


El Lenguaje de Marcado Vectorial se usa para definir la forma.

 **Remarks:** 

Un formato obsoleto incluido en Office Open XML solo por razones heredadas.

### length {#length}
```
public static int length
```


### fromName(String shapeMarkupLanguageName) {#fromName-java.lang.String}
```
public static byte fromName(String shapeMarkupLanguageName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeMarkupLanguageName | java.lang.String |  |

**Returns:**
byte
### getName(byte shapeMarkupLanguage) {#getName-byte}
```
public static String getName(byte shapeMarkupLanguage)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
