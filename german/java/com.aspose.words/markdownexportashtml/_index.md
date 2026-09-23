---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen der Elemente, die in Java als rohes HTML in Markdown exportiert werden sollen."
type: docs
weight: 451
url: /de/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Ermöglicht die Angabe der Elemente, die als rohes HTML nach Markdown exportiert werden sollen.

 **Examples:** 

Zeigt, wie man eine Tabelle als rohes HTML in Markdown exportiert.

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

Zeigt, wie man Tabellen, die in reinem Markdown nicht korrekt dargestellt werden können, als rohes HTML exportiert.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [NONE](#NONE) | Exportiere alle Elemente mit Markdown-Syntax ohne jegliches rohes HTML. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Exportiere Tabellen, die in reinem Markdown nicht korrekt dargestellt werden können, als rohes HTML. |
| [TABLES](#TABLES) | Exportiere Tabellen als rohes HTML. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
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


Exportiere alle Elemente mit Markdown-Syntax ohne jegliches rohes HTML.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Exportiere Tabellen, die in reinem Markdown nicht korrekt dargestellt werden können, als rohes HTML.

 **Remarks:** 

Wenn diese Option aktiviert ist, exportiert Aspose.Words nur Tabellen mit zusammengeführten Zellen oder verschachtelten Tabellen als rohes HTML. Alle anderen Tabellen werden im Markdown-Format exportiert. Beachten Sie außerdem, dass diese Option nicht die gesamte Formatierung der Tabelle beibehält, sondern nur die entsprechenden Zellbereiche.

Wenn das zugehörige [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES)-Flag gesetzt ist, wird dieses Flag ignoriert.

### TABLES {#TABLES}
```
public static int TABLES
```


Exportiere Tabellen als rohes HTML.

 **Remarks:** 

Wenn diese Option aktiviert ist, wird jede Tabelle als rohes HTML exportiert. Aspose.Words wird in diesem Fall versuchen, die gesamte Formatierung der Tabellen beizubehalten.

Wenn dieses Flag gesetzt ist, wird das zugehörige [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES)-Flag ignoriert.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
