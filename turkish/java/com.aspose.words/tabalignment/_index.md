---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da bir sekme durağının hizalamasını/türünü belirtir."
type: docs
weight: 652
url: /tr/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Bir sekme durağının hizalamasını/tipini belirtir.

 **Examples:** 

Bir paragraf için özel sekme durakları nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // If we are in a paragraph with no tab stops in this collection,
 // the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
 Assert.assertEquals(0, doc.getFirstSection().getBody().getFirstParagraph().getEffectiveTabStops().length);

 // We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
 // Each unit on this ruler is two default tab stops, which is 72 points.
 // We can add custom tab stops programmatically like this.
 TabStopCollection tabStops = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getTabStops();
 tabStops.add(72.0, TabAlignment.LEFT, TabLeader.DOTS);
 tabStops.add(216.0, TabAlignment.CENTER, TabLeader.DASHES);
 tabStops.add(360.0, TabAlignment.RIGHT, TabLeader.LINE);

 // We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
 Assert.assertEquals(3, para.getEffectiveTabStops().length);

 // Any tab characters we add will make use of the tab stops on the ruler and may,
 // depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
 para.appendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

 doc.save(getArtifactsDir() + "Paragraph.TabStops.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BAR](#BAR) | Sekme durağı konumunda dikey bir çubuk çizer. |
| [CENTER](#CENTER) | Metni sekme durağı etrafında ortalar. |
| [CLEAR](#CLEAR) | Bu konumdaki tüm sekme duraklarını temizler. |
| [DECIMAL](#DECIMAL) | Metni ondalık noktada hizalar. |
| [LEFT](#LEFT) | Sekme durakından sonraki metni sola hizalar. |
| [LIST](#LIST) | Sekme, bir liste öğesindeki sayı/işaret ve metin arasındaki ayırıcıdır. |
| [RIGHT](#RIGHT) | Sekme durakında metni sağa hizalar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Sekme durağı konumunda dikey bir çubuk çizer.

### CENTER {#CENTER}
```
public static int CENTER
```


Metni sekme durağı etrafında ortalar.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Bu konumdaki tüm sekme duraklarını temizler.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Metni ondalık noktada hizalar.

### LEFT {#LEFT}
```
public static int LEFT
```


Sekme durakından sonraki metni sola hizalar.

### LIST {#LIST}
```
public static int LIST
```


Sekme, bir liste öğesindeki sayı/işaret ve metin arasındaki ayırıcıdır.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Sekme durakında metni sağa hizalar.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tabAlignment) {#toString-int}
```
public static String toString(int tabAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
