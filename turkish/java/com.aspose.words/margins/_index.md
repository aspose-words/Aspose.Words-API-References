---
title: "Kenar boşlukları"
linktitle: "Kenar boşlukları"
second_title: "Aspose.Words Java için"
description: "Java'da önceden tanımlı kenar boşluklarını belirtir."
type: docs
weight: 449
url: /tr/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Önceden ayarlanmış kenar boşluklarını belirtir.

 **Examples:** 

Belgenin sayfa yerleşimini ne zaman yeniden hesaplayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CUSTOM](#CUSTOM) | Özel kenar boşlukları. |
| [MIRRORED](#MIRRORED) | Yansıtılmış kenar boşlukları. |
| [MODERATE](#MODERATE) | Orta kenar boşlukları. |
| [NARROW](#NARROW) | Dar kenar boşlukları. |
| [NORMAL](#NORMAL) | Normal kenar boşlukları. |
| [WIDE](#WIDE) | Geniş kenar boşlukları. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Özel kenar boşlukları.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Yansıtılmış kenar boşlukları.

 **Remarks:** 

Kenar boşluklarını Mirrored olarak ayarlamak, [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\\#setMultiplePages-int) özelliği için uygun değeri ayarlar. Bu, yalnızca geçerli bölümü değil, tüm belgeyi etkiler.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Orta kenar boşlukları.

### NARROW {#NARROW}
```
public static int NARROW
```


Dar kenar boşlukları.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal kenar boşlukları.

### WIDE {#WIDE}
```
public static int WIDE
```


Geniş kenar boşlukları.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
