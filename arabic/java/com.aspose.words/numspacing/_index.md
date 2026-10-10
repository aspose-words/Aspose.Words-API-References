---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words لـ Java"
description: "يحدد القيم الممكنة التي يمكن عرض تباعد الأرقام بها في Java."
type: docs
weight: 484
url: /ar/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

يحدد القيم الممكنة التي يمكن عرض تباعد الأرقام فيها.

 **Examples:** 

يوضح كيفية تعيين نوع تباعد الرقم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | يحدد أن الأرقام تُعرض بالشكل الافتراضي للخط. |
| [PROPORTIONAL](#PROPORTIONAL) | يحدد أن أشكال الأرقام المصممة كمتباعدة نسبياً تُعرض إذا كان الخط يدعم ذلك. |
| [TABULAR](#TABULAR) | يحدد أن أشكال الأرقام المصممة كجدولية تُعرض إذا كان الخط يدعم ذلك. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يحدد أن الأرقام تُعرض بالشكل الافتراضي للخط.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


يحدد أن أشكال الأرقام المصممة كمتباعدة نسبياً تُعرض إذا كان الخط يدعم ذلك.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


يحدد أن أشكال الأرقام المصممة كجدولية تُعرض إذا كان الخط يدعم ذلك.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numSpacing) {#toString-int}
```
public static String toString(int numSpacing)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
