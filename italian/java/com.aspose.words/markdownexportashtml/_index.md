---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words per Java"
description: "Consente di specificare gli elementi da esportare in Markdown come HTML grezzo in Java."
type: docs
weight: 451
url: /it/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Consente di specificare gli elementi da esportare in Markdown come HTML grezzo.

 **Examples:** 

Mostra come esportare una tabella in Markdown come HTML grezzo.

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

Mostra come esportare tabelle che non possono essere rappresentate correttamente in Markdown puro come HTML grezzo.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [NONE](#NONE) | Esporta tutti gli elementi usando la sintassi Markdown senza alcun HTML grezzo. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Esporta tabelle che non possono essere rappresentate correttamente in Markdown puro come HTML grezzo. |
| [TABLES](#TABLES) | Esporta tabelle come HTML grezzo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
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


Esporta tutti gli elementi usando la sintassi Markdown senza alcun HTML grezzo.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Esporta tabelle che non possono essere rappresentate correttamente in Markdown puro come HTML grezzo.

 **Remarks:** 

Quando questa opzione è abilitata, Aspose.Words esporterà solo le tabelle che hanno celle unite o tabelle nidificate come HTML grezzo. Tutte le altre tabelle saranno esportate in formato Markdown. Inoltre, nota che questa opzione non preserva tutta la formattazione della tabella, ma conserva solo gli span corrispondenti delle celle.

Se il flag [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) correlato è impostato, questo flag verrà ignorato.

### TABLES {#TABLES}
```
public static int TABLES
```


Esporta tabelle come HTML grezzo.

 **Remarks:** 

Quando questa opzione è abilitata, ogni tabella sarà esportata come HTML grezzo. Aspose.Words cercherà di preservare tutta la formattazione delle tabelle in questo caso.

Se questo flag è impostato, il flag [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) correlato verrà ignorato.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
