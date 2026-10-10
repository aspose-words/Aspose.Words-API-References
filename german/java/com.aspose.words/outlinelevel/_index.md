---
title: "OutlineLevel"
linktitle: "OutlineLevel"
second_title: "Aspose.Words für Java"
description: "Gibt die Gliederungsebene eines Absatzes im Dokument in Java an."
type: docs
weight: 508
url: /de/java/com.aspose.words/outlinelevel/
---

**Inheritance:**
java.lang.Object
```
public class OutlineLevel
```

Gibt die Gliederungsebene eines Absatzes im Dokument an.

 **Examples:** 

Zeigt, wie Absatz-Gliederungsebenen konfiguriert werden, um zusammenklappbaren Text zu erstellen.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BODY_TEXT](#BODY-TEXT) | Der Absatz befindet sich auf der Ebene des Haupttextes. |
| [LEVEL_1](#LEVEL-1) | Der Absatz befindet sich auf Gliederungsebene 1 (höchste Ebene). |
| [LEVEL_2](#LEVEL-2) | Der Absatz befindet sich auf Gliederungsebene 2. |
| [LEVEL_3](#LEVEL-3) | Der Absatz befindet sich auf Gliederungsebene 3. |
| [LEVEL_4](#LEVEL-4) | Der Absatz befindet sich auf Gliederungsebene 4. |
| [LEVEL_5](#LEVEL-5) | Der Absatz befindet sich auf Gliederungsebene 5. |
| [LEVEL_6](#LEVEL-6) | Der Absatz befindet sich auf Gliederungsebene 6. |
| [LEVEL_7](#LEVEL-7) | Der Absatz befindet sich auf Gliederungsebene 7. |
| [LEVEL_8](#LEVEL-8) | Der Absatz befindet sich auf Gliederungsebene 8. |
| [LEVEL_9](#LEVEL-9) | Der Absatz befindet sich auf Gliederungsebene 9. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String outlineLevelName)](#fromName-java.lang.String) |  |
| [getName(int outlineLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int outlineLevel)](#toString-int) |  |
### BODY_TEXT {#BODY-TEXT}
```
public static int BODY_TEXT
```


Der Absatz befindet sich auf der Ebene des Haupttextes.

### LEVEL_1 {#LEVEL-1}
```
public static int LEVEL_1
```


Der Absatz befindet sich auf Gliederungsebene 1 (höchste Ebene).

### LEVEL_2 {#LEVEL-2}
```
public static int LEVEL_2
```


Der Absatz befindet sich auf Gliederungsebene 2.

### LEVEL_3 {#LEVEL-3}
```
public static int LEVEL_3
```


Der Absatz befindet sich auf Gliederungsebene 3.

### LEVEL_4 {#LEVEL-4}
```
public static int LEVEL_4
```


Der Absatz befindet sich auf Gliederungsebene 4.

### LEVEL_5 {#LEVEL-5}
```
public static int LEVEL_5
```


Der Absatz befindet sich auf Gliederungsebene 5.

### LEVEL_6 {#LEVEL-6}
```
public static int LEVEL_6
```


Der Absatz befindet sich auf Gliederungsebene 6.

### LEVEL_7 {#LEVEL-7}
```
public static int LEVEL_7
```


Der Absatz befindet sich auf Gliederungsebene 7.

### LEVEL_8 {#LEVEL-8}
```
public static int LEVEL_8
```


Der Absatz befindet sich auf Gliederungsebene 8.

### LEVEL_9 {#LEVEL-9}
```
public static int LEVEL_9
```


Der Absatz befindet sich auf Gliederungsebene 9.

### length {#length}
```
public static int length
```


### fromName(String outlineLevelName) {#fromName-java.lang.String}
```
public static int fromName(String outlineLevelName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outlineLevelName | java.lang.String |  |

**Returns:**
int
### getName(int outlineLevel) {#getName-int}
```
public static String getName(int outlineLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outlineLevel | int |  |

**Returns:**
java.lang.String
