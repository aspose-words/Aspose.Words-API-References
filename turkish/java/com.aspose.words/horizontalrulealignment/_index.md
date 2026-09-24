---
title: "HorizontalRuleAlignment"
linktitle: "HorizontalRuleAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da belirtilen yatay kuralın hizalamasını temsil eder."
type: docs
weight: 375
url: /tr/java/com.aspose.words/horizontalrulealignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleAlignment
```

Belirtilen yatay kural için hizalamayı temsil eder.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CENTER](#CENTER) | Ortaya hizalı. |
| [LEFT](#LEFT) | Sola hizalı. |
| [RIGHT](#RIGHT) | Sağa hizalı. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String horizontalRuleAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalRuleAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalRuleAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Ortaya hizalı.

### LEFT {#LEFT}
```
public static int LEFT
```


Sola hizalı.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Sağa hizalı.

### length {#length}
```
public static int length
```


### fromName(String horizontalRuleAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalRuleAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| horizontalRuleAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalRuleAlignment) {#getName-int}
```
public static String getName(int horizontalRuleAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
