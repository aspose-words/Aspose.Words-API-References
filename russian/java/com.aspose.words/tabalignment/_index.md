---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает выравнивание/тип табуляции в Java."
type: docs
weight: 652
url: /ru/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Указывает выравнивание/тип табуляции.

 **Examples:** 

Показывает, как задать пользовательские табуляции для абзаца.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BAR](#BAR) | Рисует вертикальную черту в позиции табуляции. |
| [CENTER](#CENTER) | Центрирует текст вокруг табуляции. |
| [CLEAR](#CLEAR) | Очищает любую табуляцию в этой позиции. |
| [DECIMAL](#DECIMAL) | Выравнивает текст по десятичной точке. |
| [LEFT](#LEFT) | Выравнивает текст по левому краю после табуляции. |
| [LIST](#LIST) | Табуляция служит разделителем между номером/маркером и текстом в элементе списка. |
| [RIGHT](#RIGHT) | Выравнивает текст по правому краю в позиции табуляции. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Рисует вертикальную черту в позиции табуляции.

### CENTER {#CENTER}
```
public static int CENTER
```


Центрирует текст вокруг табуляции.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Очищает любую табуляцию в этой позиции.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Выравнивает текст по десятичной точке.

### LEFT {#LEFT}
```
public static int LEFT
```


Выравнивает текст по левому краю после табуляции.

### LIST {#LIST}
```
public static int LIST
```


Табуляция служит разделителем между номером/маркером и текстом в элементе списка.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Выравнивает текст по правому краю в позиции табуляции.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
