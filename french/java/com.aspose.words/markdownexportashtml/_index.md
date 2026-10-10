---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut en Java."
type: docs
weight: 451
url: /fr/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut.

 **Examples:** 

Montre comment exporter un tableau vers Markdown en tant que HTML brut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

Montre comment exporter des tableaux qui ne peuvent pas être correctement représentés en Markdown pur en tant que HTML brut.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [NONE](#NONE) | Exporter tous les éléments en utilisant la syntaxe Markdown sans aucun HTML brut. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Exporter des tableaux qui ne peuvent pas être correctement représentés en Markdown pur en tant que HTML brut. |
| [TABLES](#TABLES) | Exporter les tableaux en HTML brut. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String markdownExportAsHtmlName)](#fromName-java.lang.String) |  |
| [fromNames(Set markdownExportAsHtmlNames)](#fromNames-java.util.Set) |  |
| [getName(int markdownExportAsHtml)](#getName-int) |  |
| [getNames(int markdownExportAsHtml)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownExportAsHtml)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Exporter tous les éléments en utilisant la syntaxe Markdown sans aucun HTML brut.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Exporter des tableaux qui ne peuvent pas être correctement représentés en Markdown pur en tant que HTML brut.

 **Remarks:** 

Lorsque cette option est activée, Aspose.Words n'exportera que les tableaux contenant des cellules fusionnées ou des tableaux imbriqués en HTML brut. Tous les autres tableaux seront exportés au format Markdown. Notez également que cette option ne préserve pas toute la mise en forme du tableau, mais ne conserve que les plages correspondantes des cellules.

Si le drapeau [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) associé est défini, alors ce drapeau sera ignoré.

### TABLES {#TABLES}
```
public static int TABLES
```


Exporter les tableaux en HTML brut.

 **Remarks:** 

Lorsque cette option est activée, chaque tableau sera exporté en HTML brut. Aspose.Words tentera de préserver toute la mise en forme des tableaux dans ce cas.

Si ce drapeau est défini, alors le drapeau [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) associé sera ignoré.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownExportAsHtml) {#toString-int}
```
public static String toString(int markdownExportAsHtml)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
