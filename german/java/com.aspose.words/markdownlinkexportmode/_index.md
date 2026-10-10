---
title: "MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Links in Markdown in Java exportiert werden."
type: docs
weight: 452
url: /de/java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

Gibt an, wie Links nach Markdown exportiert werden.

 **Examples:** 

Zeigt, wie Links in die .md-Datei geschrieben werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Ermittelt automatisch den Exportmodus für jeden Link. |
| [INLINE](#INLINE) | Exportiere alle Links als Inline-Blöcke. |
| [REFERENCE](#REFERENCE) | Exportiere alle Links als Referenzblöcke. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Ermittelt automatisch den Exportmodus für jeden Link.

### INLINE {#INLINE}
```
public static int INLINE
```


Exportiere alle Links als Inline-Blöcke.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Exportiere alle Links als Referenzblöcke.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
