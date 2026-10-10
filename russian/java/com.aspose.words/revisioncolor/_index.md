---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words для Java"
description: "Позволяет указать цвет исправлений документа в Java."
type: docs
weight: 581
url: /ru/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Позволяет указать цвет ревизий документа.

 **Examples:** 

Показывает, как изменить внешний вид ревизий в отрендеренном выходном документе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | По умолчанию. |
| [BLACK](#BLACK) | Представляет цвет 000000. |
| [BLUE](#BLUE) | Представляет цвет 2e97d3. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | Представляет цвет 84a35b. |
| [BY_AUTHOR](#BY-AUTHOR) | Исправления каждого автора получают собственный цвет для выделения из предопределённого набора контрастных цветов. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | Представляет цвет 0000ff. |
| [CLASSIC_RED](#CLASSIC-RED) | Представляет цвет ff0000. |
| [DARK_BLUE](#DARK-BLUE) | Представляет цвет 376e96. |
| [DARK_RED](#DARK-RED) | Представляет цвет 881824. |
| [DARK_YELLOW](#DARK-YELLOW) | Представляет цвет e09a2b. |
| [GRAY](#GRAY) | Представляет цвет efeded. |
| [GRAY_25](#GRAY-25) | Представляет цвет a0a3a9. |
| [GRAY_50](#GRAY-50) | Представляет цвет 50565e. |
| [GREEN](#GREEN) | Представляет цвет 2c6234. |
| [LIGHT_BLUE](#LIGHT-BLUE) | Представляет цвет e1f2fa. |
| [LIGHT_GREEN](#LIGHT-GREEN) | Представляет цвет e9f8ce. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | Представляет цвет fce3d0. |
| [LIGHT_PINK](#LIGHT-PINK) | Представляет цвет fce6f4. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | Представляет цвет eadfef. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | Представляет цвет fef4de. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | Для выделения изменений исправлений цвет не используется. |
| [PINK](#PINK) | Представляет цвет ce338f. |
| [RED](#RED) | Представляет цвет b5082e. |
| [TEAL](#TEAL) | Представляет цвет 1b9cab. |
| [TURQUOISE](#TURQUOISE) | Представляет цвет 3eafc2. |
| [VIOLET](#VIOLET) | Представляет цвет 633277. |
| [WHITE](#WHITE) | Представляет цвет ffffff. |
| [YELLOW](#YELLOW) | Представляет цвет fad272. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


По умолчанию.

### BLACK {#BLACK}
```
public static int BLACK
```


Представляет цвет 000000.

### BLUE {#BLUE}
```
public static int BLUE
```


Представляет цвет 2e97d3.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


Представляет цвет 84a35b.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Исправления каждого автора получают собственный цвет для выделения из предопределённого набора контрастных цветов.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


Представляет цвет 0000ff.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


Представляет цвет ff0000.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


Представляет цвет 376e96.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


Представляет цвет 881824.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


Представляет цвет e09a2b.

### GRAY {#GRAY}
```
public static int GRAY
```


Представляет цвет efeded.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


Представляет цвет a0a3a9.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


Представляет цвет 50565e.

### GREEN {#GREEN}
```
public static int GREEN
```


Представляет цвет 2c6234.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


Представляет цвет e1f2fa.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


Представляет цвет e9f8ce.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


Представляет цвет fce3d0.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


Представляет цвет fce6f4.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


Представляет цвет eadfef.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


Представляет цвет fef4de.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


Для выделения изменений исправлений цвет не используется.

### PINK {#PINK}
```
public static int PINK
```


Представляет цвет ce338f.

### RED {#RED}
```
public static int RED
```


Представляет цвет b5082e.

### TEAL {#TEAL}
```
public static int TEAL
```


Представляет цвет 1b9cab.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


Представляет цвет 3eafc2.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


Представляет цвет 633277.

### WHITE {#WHITE}
```
public static int WHITE
```


Представляет цвет ffffff.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


Представляет цвет fad272.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int revisionColor) {#toString-int}
```
public static String toString(int revisionColor)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
