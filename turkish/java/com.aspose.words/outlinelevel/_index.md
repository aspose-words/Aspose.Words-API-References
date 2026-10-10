---
title: "OutlineLevel"
linktitle: "OutlineLevel"
second_title: "Aspose.Words Java için"
description: "Java'da belgede bir paragrafın anahat seviyesini belirtir."
type: docs
weight: 508
url: /tr/java/com.aspose.words/outlinelevel/
---

**Inheritance:**
java.lang.Object
```
public class OutlineLevel
```

Belgedeki bir paragrafın taslak seviyesini belirtir.

 **Examples:** 

Paragraf anahat seviyelerini yapılandırarak katlanabilir metin oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BODY_TEXT](#BODY-TEXT) | Paragraf, ana metin seviyesinde. |
| [LEVEL_1](#LEVEL-1) | Paragraf, anahat seviyesi 1'de (en üst seviye). |
| [LEVEL_2](#LEVEL-2) | Paragraf, anahat seviyesi 2'de. |
| [LEVEL_3](#LEVEL-3) | Paragraf, anahat seviyesi 3'de. |
| [LEVEL_4](#LEVEL-4) | Paragraf, anahat seviyesi 4'de. |
| [LEVEL_5](#LEVEL-5) | Paragraf, anahat seviyesi 5'de. |
| [LEVEL_6](#LEVEL-6) | Paragraf, anahat seviyesi 6'de. |
| [LEVEL_7](#LEVEL-7) | Paragraf, anahat seviyesi 7'de. |
| [LEVEL_8](#LEVEL-8) | Paragraf, taslak seviyesi 8'de. |
| [LEVEL_9](#LEVEL-9) | Paragraf, taslak seviyesi 9'da. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String outlineLevelName)](#fromName-java.lang.String) |  |
| [getName(int outlineLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int outlineLevel)](#toString-int) |  |
### BODY_TEXT {#BODY-TEXT}
```
public static int BODY_TEXT
```


Paragraf, ana metin seviyesinde.

### LEVEL_1 {#LEVEL-1}
```
public static int LEVEL_1
```


Paragraf, anahat seviyesi 1'de (en üst seviye).

### LEVEL_2 {#LEVEL-2}
```
public static int LEVEL_2
```


Paragraf, anahat seviyesi 2'de.

### LEVEL_3 {#LEVEL-3}
```
public static int LEVEL_3
```


Paragraf, anahat seviyesi 3'de.

### LEVEL_4 {#LEVEL-4}
```
public static int LEVEL_4
```


Paragraf, anahat seviyesi 4'de.

### LEVEL_5 {#LEVEL-5}
```
public static int LEVEL_5
```


Paragraf, anahat seviyesi 5'de.

### LEVEL_6 {#LEVEL-6}
```
public static int LEVEL_6
```


Paragraf, anahat seviyesi 6'de.

### LEVEL_7 {#LEVEL-7}
```
public static int LEVEL_7
```


Paragraf, anahat seviyesi 7'de.

### LEVEL_8 {#LEVEL-8}
```
public static int LEVEL_8
```


Paragraf, taslak seviyesi 8'de.

### LEVEL_9 {#LEVEL-9}
```
public static int LEVEL_9
```


Paragraf, taslak seviyesi 9'da.

### length {#length}
```
public static int length
```


### fromName(String outlineLevelName) {#fromName-java.lang.String}
```
public static int fromName(String outlineLevelName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| outlineLevelName | java.lang.String |  |

**Returns:**
int
### getName(int outlineLevel) {#getName-int}
```
public static String getName(int outlineLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| outlineLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int outlineLevel) {#toString-int}
```
public static String toString(int outlineLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| outlineLevel | int |  |

**Returns:**
java.lang.String
