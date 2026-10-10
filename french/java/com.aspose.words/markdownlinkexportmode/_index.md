---
title: "MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les liens sont exportés vers Markdown en Java."
type: docs
weight: 452
url: /fr/java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

Spécifie comment les liens sont exportés vers Markdown.

 **Examples:** 

Montre comment les liens seront écrits dans le fichier .md.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Détecte automatiquement le mode d'exportation pour chaque lien. |
| [INLINE](#INLINE) | Exportez tous les liens en blocs en ligne. |
| [REFERENCE](#REFERENCE) | Exportez tous les liens en blocs de référence. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Détecte automatiquement le mode d'exportation pour chaque lien.

### INLINE {#INLINE}
```
public static int INLINE
```


Exportez tous les liens en blocs en ligne.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Exportez tous les liens en blocs de référence.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
