---
title: "HorizontalRuleAlignment"
linktitle: "HorizontalRuleAlignment"
second_title: "Aspose.Words für Java"
description: "Stellt die Ausrichtung der angegebenen horizontalen Regel in Java dar."
type: docs
weight: 375
url: /de/java/com.aspose.words/horizontalrulealignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleAlignment
```

Stellt die Ausrichtung für die angegebene horizontale Linie dar.

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CENTER](#CENTER) | Zentriert ausgerichtet. |
| [LEFT](#LEFT) | Linksbündig ausgerichtet. |
| [RIGHT](#RIGHT) | Rechtsbündig ausgerichtet. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String horizontalRuleAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalRuleAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalRuleAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Zentriert ausgerichtet.

### LEFT {#LEFT}
```
public static int LEFT
```


Linksbündig ausgerichtet.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Rechtsbündig ausgerichtet.

### length {#length}
```
public static int length
```


### fromName(String horizontalRuleAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalRuleAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalRuleAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalRuleAlignment) {#getName-int}
```
public static String getName(int horizontalRuleAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalRuleAlignment) {#toString-int}
```
public static String toString(int horizontalRuleAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
