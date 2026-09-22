---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words لـ Java"
description: "يحدد الأنواع الممكنة لعلامة التشديد في جافا."
type: docs
weight: 187
url: /ar/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

يحدد الأنواع الممكنة لعلامة التأكيد.

 **Examples:** 

يعرض كيفية إضافة حرف إضافي يُعرض فوق/تحت حرف الشكل.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [NONE](#NONE) | بدون علامة تشديد. |
| [OVER_COMMA](#OVER-COMMA) | علامة التشديد هي حرف فاصلة يُعرض فوق النص. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | علامة التشديد هي دائرة سوداء صلبة تُعرض فوق النص. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | علامة التشديد هي دائرة بيضاء فارغة تُعرض فوق النص. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | علامة التشديد هي دائرة سوداء صلبة تُعرض أسفل النص. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


بدون علامة تشديد.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


علامة التشديد هي حرف فاصلة يُعرض فوق النص.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


علامة التشديد هي دائرة سوداء صلبة تُعرض فوق النص.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


علامة التشديد هي دائرة بيضاء فارغة تُعرض فوق النص.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


علامة التشديد هي دائرة سوداء صلبة تُعرض أسفل النص.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
