---
title: "OoxmlCompliance"
linktitle: "OoxmlCompliance"
second_title: "Aspose.Words para Java"
description: "Permite especificar qué especificación OOXML se utilizará al guardar en formato DOCX en Java."
type: docs
weight: 503
url: /es/java/com.aspose.words/ooxmlcompliance/
---

**Inheritance:**
java.lang.Object
```
public class OoxmlCompliance
```

Permite especificar qué especificación OOXML se utilizará al guardar en formato DOCX.

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

Muestra cómo configurar una lista para reiniciar la numeración en cada sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 List list = doc.getLists().get(0);
 list.isRestartAtEachSection(restartListAtEachSection);

 // The "IsRestartAtEachSection" property will only be applicable when
 // the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
 OoxmlSaveOptions options = new OoxmlSaveOptions();
 {
     options.setCompliance(OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);
 }

 builder.getListFormat().setList(list);

 builder.writeln("List item 1");
 builder.writeln("List item 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("List item 3");
 builder.writeln("List item 4");

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.RestartingDocumentList.docx");

 Assert.assertEquals(restartListAtEachSection, doc.getLists().get(0).isRestartAtEachSection());
 
```

Muestra cómo insertar formas DML en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two wrapping types that shapes may have.
 // 1 -  Floating:
 builder.insertShape(ShapeType.TOP_CORNERS_ROUNDED, RelativeHorizontalPosition.PAGE, 100.0,
         RelativeVerticalPosition.PAGE, 100.0, 50.0, 50.0, WrapType.NONE);

 // 2 -  Inline:
 builder.insertShape(ShapeType.DIAGONAL_CORNERS_ROUNDED, 50.0, 50.0);

 // If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
 // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
 // then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);

 doc.save(getArtifactsDir() + "Shape.ShapeInsertion.docx", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ECMA_376_2006](#ECMA-376-2006) | ECMA-376 1ª Edición, 2006. |
| [ISO_29500_2008_STRICT](#ISO-29500-2008-STRICT) | Nivel de cumplimiento estricto ISO/IEC 29500:2008. |
| [ISO_29500_2008_TRANSITIONAL](#ISO-29500-2008-TRANSITIONAL) | Nivel de cumplimiento transicional ISO/IEC 29500:2008. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String ooxmlComplianceName)](#fromName-java.lang.String) |  |
| [getName(int ooxmlCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int ooxmlCompliance)](#toString-int) |  |
### ECMA_376_2006 {#ECMA-376-2006}
```
public static int ECMA_376_2006
```


ECMA-376 1ª Edición, 2006.

### ISO_29500_2008_STRICT {#ISO-29500-2008-STRICT}
```
public static int ISO_29500_2008_STRICT
```


Nivel de cumplimiento estricto ISO/IEC 29500:2008.

### ISO_29500_2008_TRANSITIONAL {#ISO-29500-2008-TRANSITIONAL}
```
public static int ISO_29500_2008_TRANSITIONAL
```


Nivel de cumplimiento transicional ISO/IEC 29500:2008.

### length {#length}
```
public static int length
```


### fromName(String ooxmlComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String ooxmlComplianceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ooxmlComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int ooxmlCompliance) {#getName-int}
```
public static String getName(int ooxmlCompliance)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ooxmlCompliance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int ooxmlCompliance) {#toString-int}
```
public static String toString(int ooxmlCompliance)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ooxmlCompliance | int |  |

**Returns:**
java.lang.String
