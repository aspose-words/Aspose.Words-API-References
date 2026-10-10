---
title: "LineSpacingRule"
linktitle: "LineSpacingRule"
second_title: "Aspose.Words para Java"
description: "Especifica los valores de interlineado para un párrafo en Java."
type: docs
weight: 423
url: /es/java/com.aspose.words/linespacingrule/
---

**Inheritance:**
java.lang.Object
```
public class LineSpacingRule
```

Especifica los valores de interlineado para un párrafo.

 **Examples:** 

Muestra cómo trabajar con el interlineado.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | El interlineado puede ser mayor o igual, pero nunca menor que el valor especificado en la propiedad [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double). |
| [EXACTLY](#EXACTLY) | El interlineado nunca cambia del valor especificado en la propiedad [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), incluso si se usa una fuente más grande dentro del párrafo. |
| [MULTIPLE](#MULTIPLE) | El interlineado se especifica en la propiedad [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) como el número de líneas. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String) |  |
| [getName(int lineSpacingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineSpacingRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


El interlineado puede ser mayor o igual, pero nunca menor que el valor especificado en la propiedad [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


El interlineado nunca cambia del valor especificado en la propiedad [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), incluso si se usa una fuente más grande dentro del párrafo.

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


El interlineado se especifica en la propiedad [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) como el número de líneas. Una línea equivale a 12 puntos.

### length {#length}
```
public static int length
```


### fromName(String lineSpacingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String lineSpacingRuleName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**Returns:**
int
### getName(int lineSpacingRule) {#getName-int}
```
public static String getName(int lineSpacingRule)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| lineSpacingRule | int |  |

**Returns:**
java.lang.String
