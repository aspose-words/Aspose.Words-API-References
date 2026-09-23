---
title: "HtmlElementSizeOutputMode"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments vers HTML, MHTML et EPUB en Java."
type: docs
weight: 378
url: /fr/java/com.aspose.words/htmlelementsizeoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments vers HTML, MHTML et EPUB.

 **Examples:** 

Montre comment préserver les retraits négatifs dans le .html de sortie.

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
## Champs

| Champ | Description |
| --- | --- |
| [ALL](#ALL) | Toutes les tailles d'éléments, à la fois en unités absolues et relatives, spécifiées dans le document sont exportées. |
| [NONE](#NONE) | Les tailles d'éléments ne sont pas exportées. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Les tailles d'éléments sont exportées uniquement si elles sont spécifiées en unités relatives dans le document. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Toutes les tailles d'éléments, à la fois en unités absolues et relatives, spécifiées dans le document sont exportées.

### NONE {#NONE}
```
public static int NONE
```


Les tailles d'élément ne sont pas exportées. Les agents visuels construiront la mise en page automatiquement en fonction de la relation entre les éléments.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Les tailles d'élément ne sont exportées que si elles sont spécifiées en unités relatives dans le document. Les tailles fixes ne sont pas exportées dans ce mode. Les agents visuels calculeront les tailles manquantes pour rendre la mise en page du document plus naturelle.

### length {#length}
```
public static int length
```


### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlElementSizeOutputMode) {#getName-int}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
