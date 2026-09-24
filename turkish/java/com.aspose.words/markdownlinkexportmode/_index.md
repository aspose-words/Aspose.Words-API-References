---
title: "MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words Java için"
description: "Java'da bağlantıların Markdown'a nasıl dışa aktarılacağını belirtir."
type: docs
weight: 452
url: /tr/java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

Bağlantıların Markdown'a nasıl dışa aktarıldığını belirtir.

 **Examples:** 

Bağlantıların .md dosyasına nasıl yazılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Her bağlantı için dışa aktarma modunu otomatik olarak algılar. |
| [INLINE](#INLINE) | Tüm bağlantıları satır içi bloklar olarak dışa aktar. |
| [REFERENCE](#REFERENCE) | Tüm bağlantıları referans blokları olarak dışa aktar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Her bağlantı için dışa aktarma modunu otomatik olarak algılar.

### INLINE {#INLINE}
```
public static int INLINE
```


Tüm bağlantıları satır içi bloklar olarak dışa aktar.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Tüm bağlantıları referans blokları olarak dışa aktar.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
