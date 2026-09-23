---
title: "MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words per Java"
description: "Specifica come i collegamenti vengono esportati in Markdown in Java."
type: docs
weight: 452
url: /it/java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

Specifica come i collegamenti vengono esportati in Markdown.

 **Examples:** 

Mostra come i collegamenti verranno scritti nel file .md.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertShape(ShapeType.BALLOON, 100.0, 100.0);

 // Image will be written as reference:
 // ![ref1]
 //
 // [ref1]: aw_ref.001.png
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.REFERENCE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

 // Image will be written as inline:
 // ![](../aw_inline.001.png)
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.INLINE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | Rileva automaticamente la modalità di esportazione per ogni collegamento. |
| [INLINE](#INLINE) | Esporta tutti i collegamenti come blocchi inline. |
| [REFERENCE](#REFERENCE) | Esporta tutti i collegamenti come blocchi di riferimento. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Rileva automaticamente la modalità di esportazione per ogni collegamento.

### INLINE {#INLINE}
```
public static int INLINE
```


Esporta tutti i collegamenti come blocchi inline.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Esporta tutti i collegamenti come blocchi di riferimento.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownLinkExportMode) {#toString-int}
```
public static String toString(int markdownLinkExportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
