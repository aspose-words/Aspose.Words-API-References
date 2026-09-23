---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'alignement/type d'un arrêt de tabulation en Java."
type: docs
weight: 652
url: /fr/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Spécifie l'alignement/type d'un arrêt de tabulation.

 **Examples:** 

Montre comment définir des arrêts de tabulation personnalisés pour un paragraphe.

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
## Champs

| Champ | Description |
| --- | --- |
| [BAR](#BAR) | Dessine une barre verticale à la position de l'arrêt de tabulation. |
| [CENTER](#CENTER) | Centre le texte autour de l'arrêt de tabulation. |
| [CLEAR](#CLEAR) | Efface tout arrêt de tabulation à cette position. |
| [DECIMAL](#DECIMAL) | Aligne le texte sur le point décimal. |
| [LEFT](#LEFT) | Aligne le texte à gauche après l'arrêt de tabulation. |
| [LIST](#LIST) | La tabulation est un délimiteur entre le numéro/puce et le texte dans un élément de liste. |
| [RIGHT](#RIGHT) | Aligne le texte à droite à l'arrêt de tabulation. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Dessine une barre verticale à la position de l'arrêt de tabulation.

### CENTER {#CENTER}
```
public static int CENTER
```


Centre le texte autour de l'arrêt de tabulation.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Efface tout arrêt de tabulation à cette position.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Aligne le texte sur le point décimal.

### LEFT {#LEFT}
```
public static int LEFT
```


Aligne le texte à gauche après l'arrêt de tabulation.

### LIST {#LIST}
```
public static int LIST
```


La tabulation est un délimiteur entre le numéro/puce et le texte dans un élément de liste.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Aligne le texte à droite à l'arrêt de tabulation.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
