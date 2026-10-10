---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words para Java"
description: "Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar en Java."
type: docs
weight: 451
url: /es/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar.

 **Examples:** 

Muestra cómo exportar una tabla a Markdown como HTML sin procesar.

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

Muestra cómo exportar tablas que no pueden representarse correctamente en Markdown puro como HTML sin procesar.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [NONE](#NONE) | Exporta todos los elementos usando la sintaxis Markdown sin ningún HTML sin procesar. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Exporta tablas que no pueden representarse correctamente en Markdown puro como HTML sin procesar. |
| [TABLES](#TABLES) | Exporta tablas como HTML sin procesar. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
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


Exporta todos los elementos usando la sintaxis Markdown sin ningún HTML sin procesar.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Exporta tablas que no pueden representarse correctamente en Markdown puro como HTML sin procesar.

 **Remarks:** 

Cuando esta opción está habilitada, Aspose.Words solo exportará las tablas que tengan celdas combinadas o tablas anidadas como HTML sin procesar. Y todas las demás tablas se exportarán en formato Markdown. También tenga en cuenta que esta opción no preservará todo el formato de la tabla, sino solo los intervalos correspondientes de las celdas.

Si la bandera [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) relacionada está establecida, entonces esta bandera será ignorada.

### TABLES {#TABLES}
```
public static int TABLES
```


Exporta tablas como HTML sin procesar.

 **Remarks:** 

Cuando esta opción está habilitada, cada tabla se exportará como HTML sin procesar. Aspose.Words intentará preservar todo el formato de las tablas en este caso.

Si esta bandera está establecida, entonces la bandera [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) relacionada será ignorada.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
