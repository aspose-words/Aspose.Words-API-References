---
title: LineSpacingRule
linktitle: LineSpacingRule
second_title: Aspose.Words for Java
description: Specifies line spacing values for a paragraph in Java.
type: docs
weight: 414
url: /java/com.aspose.words/linespacingrule/
---

**Inheritance:**
java.lang.Object
```
public class LineSpacingRule
```

Specifies line spacing values for a paragraph.

 **Examples:** 

Shows how to work with line spacing.

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
## Fields

| Field | Description |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | The line spacing can be greater than or equal to, but never less than, the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property. |
| [EXACTLY](#EXACTLY) | The line spacing never changes from the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property, even if a larger font is used within the paragraph. |
| [MULTIPLE](#MULTIPLE) | The line spacing is specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property as the number of lines. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String) |  |
| [getName(int lineSpacingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineSpacingRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


The line spacing can be greater than or equal to, but never less than, the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


The line spacing never changes from the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property, even if a larger font is used within the paragraph.

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


The line spacing is specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property as the number of lines. One line equals 12 points.

### length {#length}
```
public static int length
```


### fromName(String lineSpacingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String lineSpacingRuleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**Returns:**
int
### getName(int lineSpacingRule) {#getName-int}
```
public static String getName(int lineSpacingRule)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| lineSpacingRule | int |  |

**Returns:**
java.lang.String
