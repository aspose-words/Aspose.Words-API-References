---
title: "HorizontalRuleAlignment"
linktitle: "HorizontalRuleAlignment"
second_title: "Aspose.Words para Java"
description: "Representa la alineación de la regla horizontal especificada en Java."
type: docs
weight: 375
url: /es/java/com.aspose.words/horizontalrulealignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleAlignment
```

Representa la alineación para la regla horizontal especificada.

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CENTER](#CENTER) | Alineado al centro. |
| [LEFT](#LEFT) | Alineado a la izquierda. |
| [RIGHT](#RIGHT) | Alineado a la derecha. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String horizontalRuleAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalRuleAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalRuleAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Alineado al centro.

### LEFT {#LEFT}
```
public static int LEFT
```


Alineado a la izquierda.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Alineado a la derecha.

### length {#length}
```
public static int length
```


### fromName(String horizontalRuleAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalRuleAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| horizontalRuleAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalRuleAlignment) {#getName-int}
```
public static String getName(int horizontalRuleAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
