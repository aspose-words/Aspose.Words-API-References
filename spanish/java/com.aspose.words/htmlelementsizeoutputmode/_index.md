---
title: "HtmlElementSizeOutputMode"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words exporta los anchos y alturas de los elementos a HTML, MHTML y EPUB en Java."
type: docs
weight: 378
url: /es/java/com.aspose.words/htmlelementsizeoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Especifica cómo Aspose.Words exporta los anchos y alturas de los elementos a HTML, MHTML y EPUB.

 **Examples:** 

Muestra cómo preservar sangrías negativas en el .html de salida.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table with a negative indent, which will push it to the left past the left page boundary.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(-36);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 // Insert a table with a positive indent, which will push the table to the right.
 table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(36.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 // When we save a document to HTML, Aspose.Words will only preserve negative indents
 // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
 // in a SaveOptions object that we will pass to "true".
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setAllowNegativeIndent(allowNegativeIndent);
     options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE_ONLY);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF_8);

 if (allowNegativeIndent) {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 else
 {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ALL](#ALL) | Todos los tamaños de los elementos, tanto en unidades absolutas como relativas, especificados en el documento se exportan. |
| [NONE](#NONE) | Los tamaños de los elementos no se exportan. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Los tamaños de los elementos se exportan solo si están especificados en unidades relativas en el documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Todos los tamaños de los elementos, tanto en unidades absolutas como relativas, especificados en el documento se exportan.

### NONE {#NONE}
```
public static int NONE
```


Los tamaños de los elementos no se exportan. Los agentes visuales crearán el diseño automáticamente según la relación entre los elementos.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Los tamaños de los elementos se exportan solo si están especificados en unidades relativas en el documento. Los tamaños fijos no se exportan en este modo. Los agentes visuales calcularán los tamaños faltantes para que el diseño del documento sea más natural.

### length {#length}
```
public static int length
```


### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlElementSizeOutputMode) {#getName-int}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlElementSizeOutputMode) {#toString-int}
```
public static String toString(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
