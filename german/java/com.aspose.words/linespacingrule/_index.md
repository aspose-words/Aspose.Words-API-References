---
title: "LineSpacingRule"
linktitle: "LineSpacingRule"
second_title: "Aspose.Words für Java"
description: "Gibt Zeilenabstandswerte für einen Absatz in Java an."
type: docs
weight: 423
url: /de/java/com.aspose.words/linespacingrule/
---

**Inheritance:**
java.lang.Object
```
public class LineSpacingRule
```

Gibt Zeilenabstandswerte für einen Absatz an.

 **Examples:** 

Zeigt, wie mit Zeilenabstand gearbeitet wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | Der Zeilenabstand kann größer oder gleich, aber niemals kleiner als der in der [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) Eigenschaft angegebene Wert sein. |
| [EXACTLY](#EXACTLY) | Der Zeilenabstand ändert sich niemals vom in der [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) Eigenschaft angegebenen Wert, selbst wenn innerhalb des Absatzes eine größere Schrift verwendet wird. |
| [MULTIPLE](#MULTIPLE) | Der Zeilenabstand wird in der [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) Eigenschaft als Anzahl der Zeilen angegeben. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String) |  |
| [getName(int lineSpacingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineSpacingRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


Der Zeilenabstand kann größer oder gleich, aber niemals kleiner als der in der [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) Eigenschaft angegebene Wert sein.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


Der Zeilenabstand ändert sich niemals vom in der [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) Eigenschaft angegebenen Wert, selbst wenn innerhalb des Absatzes eine größere Schrift verwendet wird.

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


Der Zeilenabstand wird in der [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) Eigenschaft als Anzahl der Zeilen angegeben. Eine Zeile entspricht 12 Punkten.

### length {#length}
```
public static int length
```


### fromName(String lineSpacingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String lineSpacingRuleName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**Returns:**
int
### getName(int lineSpacingRule) {#getName-int}
```
public static String getName(int lineSpacingRule)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| lineSpacingRule | int |  |

**Returns:**
java.lang.String
