---
title: "ShapeMarkupLanguage"
linktitle: "ShapeMarkupLanguage"
second_title: "Aspose.Words per Java"
description: "Specifica il linguaggio di markup utilizzato per la forma in Java."
type: docs
weight: 615
url: /it/java/com.aspose.words/shapemarkuplanguage/
---

**Inheritance:**
java.lang.Object
```
public class ShapeMarkupLanguage
```

Specifica il linguaggio di markup usato per la forma.

 **Examples:** 

Mostra come impostare una specifica di conformità OOXML a cui aderire per un documento salvato.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DML](#DML) | Il Drawing Markup Language è usato per definire la forma. |
| [VML](#VML) | Il Vector Markup Language è usato per definire la forma. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String shapeMarkupLanguageName)](#fromName-java.lang.String) |  |
| [getName(byte shapeMarkupLanguage)](#getName-byte) |  |
| [getValues()](#getValues) |  |
| [toString(byte shapeMarkupLanguage)](#toString-byte) |  |
### DML {#DML}
```
public static byte DML
```


Il Drawing Markup Language è usato per definire la forma.

 **Remarks:** 

Questo è il nuovo standard di disegno per Office Open XML, apparso per la prima volta nella prima edizione ECMA-376 (2006) e introdotto in MS Word 2007.

### VML {#VML}
```
public static byte VML
```


Il Vector Markup Language è usato per definire la forma.

 **Remarks:** 

Un formato deprecato incluso in Office Open XML solo per motivi di retrocompatibilità.

### length {#length}
```
public static int length
```


### fromName(String shapeMarkupLanguageName) {#fromName-java.lang.String}
```
public static byte fromName(String shapeMarkupLanguageName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeMarkupLanguageName | java.lang.String |  |

**Returns:**
byte
### getName(byte shapeMarkupLanguage) {#getName-byte}
```
public static String getName(byte shapeMarkupLanguage)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
