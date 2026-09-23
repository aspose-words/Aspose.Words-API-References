---
title: "HorizontalRuleAlignment"
linktitle: "HorizontalRuleAlignment"
second_title: "Aspose.Words pour Java"
description: "Représente l'alignement de la règle horizontale spécifiée en Java."
type: docs
weight: 375
url: /fr/java/com.aspose.words/horizontalrulealignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleAlignment
```

Représente l’alignement pour la règle horizontale spécifiée.

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

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
## Champs

| Champ | Description |
| --- | --- |
| [CENTER](#CENTER) | Aligné au centre. |
| [LEFT](#LEFT) | Aligné à gauche. |
| [RIGHT](#RIGHT) | Aligné à droite. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String horizontalRuleAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalRuleAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalRuleAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Aligné au centre.

### LEFT {#LEFT}
```
public static int LEFT
```


Aligné à gauche.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Aligné à droite.

### length {#length}
```
public static int length
```


### fromName(String horizontalRuleAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalRuleAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| horizontalRuleAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalRuleAlignment) {#getName-int}
```
public static String getName(int horizontalRuleAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
