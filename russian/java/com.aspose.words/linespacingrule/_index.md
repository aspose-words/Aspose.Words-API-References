---
title: "LineSpacingRule"
linktitle: "LineSpacingRule"
second_title: "Aspose.Words для Java"
description: "Указывает значения межстрочного интервала для абзаца в Java."
type: docs
weight: 423
url: /ru/java/com.aspose.words/linespacingrule/
---

**Inheritance:**
java.lang.Object
```
public class LineSpacingRule
```

Указывает значения межстрочного интервала для абзаца.

 **Examples:** 

Показывает, как работать с межстрочным интервалом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | Межстрочный интервал может быть больше или равен, но никогда меньше, значения, указанного в свойстве [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property. |
| [EXACTLY](#EXACTLY) | Межстрочный интервал никогда не меняется от значения, указанного в свойстве [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), даже если в абзаце используется более крупный шрифт. |
| [MULTIPLE](#MULTIPLE) | Межстрочный интервал задаётся в свойстве [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) как количество строк. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String) |  |
| [getName(int lineSpacingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineSpacingRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


Межстрочный интервал может быть больше или равен, но никогда меньше, значения, указанного в свойстве [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


Межстрочный интервал никогда не меняется от значения, указанного в свойстве [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), даже если в абзаце используется более крупный шрифт.

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


Межстрочный интервал задаётся в свойстве [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) как количество строк. Одна строка равна 12 пунктам.

### length {#length}
```
public static int length
```


### fromName(String lineSpacingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String lineSpacingRuleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**Returns:**
int
### getName(int lineSpacingRule) {#getName-int}
```
public static String getName(int lineSpacingRule)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| lineSpacingRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int lineSpacingRule) {#toString-int}
```
public static String toString(int lineSpacingRule)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| lineSpacingRule | int |  |

**Returns:**
java.lang.String
