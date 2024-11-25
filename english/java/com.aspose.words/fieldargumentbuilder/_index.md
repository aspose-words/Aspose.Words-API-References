---
title: FieldArgumentBuilder
linktitle: FieldArgumentBuilder
second_title: Aspose.Words for Java
description: Builds a complex field argument consisting of fields nodes and plain text in Java.
type: docs
weight: 188
url: /java/com.aspose.words/fieldargumentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class FieldArgumentBuilder
```

Builds a complex field argument consisting of fields, nodes, and plain text.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

 **Examples:** 

Shows how to construct fields using a field builder, and then insert them into the document.

```

 Document doc = new Document();

 // Below are three examples of field construction done using a field builder.
 // 1 -  Single field:
 // Use a field builder to add a SYMBOL field which displays the \u0192 (Florin) symbol.
 FieldBuilder builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(402);
 builder.addSwitch("\\f", "Arial");
 builder.addSwitch("\\s", 25);
 builder.addSwitch("\\u");
 Field field = builder.buildAndInsert(doc.getFirstSection().getBody().getFirstParagraph());

 Assert.assertEquals(field.getFieldCode(), " SYMBOL 402 \\f Arial \\s 25 \\u ");

 // 2 -  Nested field:
 // Use a field builder to create a formula field used as an inner field by another field builder.
 FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FIELD_FORMULA);
 innerFormulaBuilder.addArgument(100);
 innerFormulaBuilder.addArgument("+");
 innerFormulaBuilder.addArgument(74);

 // Create another builder for another SYMBOL field, and insert the formula field
 // that we have created above into the SYMBOL field as its argument.
 builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(innerFormulaBuilder);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 // The outer SYMBOL field will use the formula field result, 174, as its argument,
 // which will make the field display the ® (Registered Sign) symbol since its character number is 174.
 Assert.assertEquals(" SYMBOL  = 100 + 74  ", field.getFieldCode());

 // 3 -  Multiple nested fields and arguments:
 // Now, we will use a builder to create an IF field, which displays one of two custom string values,
 // depending on the true/false value of its expression. To get a true/false value
 // that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
 // We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
 FieldBuilder leftExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 leftExpression.addArgument(2);
 leftExpression.addArgument("+");
 leftExpression.addArgument(3);

 FieldBuilder rightExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 rightExpression.addArgument(2.5);
 rightExpression.addArgument("*");
 rightExpression.addArgument(5.2);

 // Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
 // These arguments will reuse the output values of our numeric expressions.
 FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
 trueOutput.addText("True, both expressions amount to ");
 trueOutput.addField(leftExpression);

 FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
 falseOutput.addNode(new Run(doc, "False, "));
 falseOutput.addField(leftExpression);
 falseOutput.addNode(new Run(doc, " does not equal "));
 falseOutput.addField(rightExpression);

 // Finally, we will create one more field builder for the IF field and combine all of the expressions.
 builder = new FieldBuilder(FieldType.FIELD_IF);
 builder.addArgument(leftExpression);
 builder.addArgument("=");
 builder.addArgument(rightExpression);
 builder.addArgument(trueOutput);
 builder.addArgument(falseOutput);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 Assert.assertEquals(" IF  = 2 + 3  =  = 2.5 * 5.2  " +
         "\"True, both expressions amount to  = 2 + 3 \" " +
         "\"False,  = 2 + 3  does not equal  = 2.5 * 5.2 \" ", field.getFieldCode());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SYMBOL.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldArgumentBuilder()](#FieldArgumentBuilder) | Initializes an instance of the [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/) class. |
## Methods

| Method | Description |
| --- | --- |
| [addField(FieldBuilder fieldBuilder)](#addField-com.aspose.words.FieldBuilder) | Adds a field represented by a [FieldBuilder](../../com.aspose.words/fieldbuilder/) to the argument. |
| [addNode(Inline node)](#addNode-com.aspose.words.Inline) | Adds a node to the argument. |
| [addText(String text)](#addText-java.lang.String) | Adds a plain text to the argument. |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder) |  |
### FieldArgumentBuilder() {#FieldArgumentBuilder}
```
public FieldArgumentBuilder()
```


Initializes an instance of the [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/) class.

 **Examples:** 

Shows how to construct fields using a field builder, and then insert them into the document.

```

 Document doc = new Document();

 // Below are three examples of field construction done using a field builder.
 // 1 -  Single field:
 // Use a field builder to add a SYMBOL field which displays the \u0192 (Florin) symbol.
 FieldBuilder builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(402);
 builder.addSwitch("\\f", "Arial");
 builder.addSwitch("\\s", 25);
 builder.addSwitch("\\u");
 Field field = builder.buildAndInsert(doc.getFirstSection().getBody().getFirstParagraph());

 Assert.assertEquals(field.getFieldCode(), " SYMBOL 402 \\f Arial \\s 25 \\u ");

 // 2 -  Nested field:
 // Use a field builder to create a formula field used as an inner field by another field builder.
 FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FIELD_FORMULA);
 innerFormulaBuilder.addArgument(100);
 innerFormulaBuilder.addArgument("+");
 innerFormulaBuilder.addArgument(74);

 // Create another builder for another SYMBOL field, and insert the formula field
 // that we have created above into the SYMBOL field as its argument.
 builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(innerFormulaBuilder);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 // The outer SYMBOL field will use the formula field result, 174, as its argument,
 // which will make the field display the ® (Registered Sign) symbol since its character number is 174.
 Assert.assertEquals(" SYMBOL  = 100 + 74  ", field.getFieldCode());

 // 3 -  Multiple nested fields and arguments:
 // Now, we will use a builder to create an IF field, which displays one of two custom string values,
 // depending on the true/false value of its expression. To get a true/false value
 // that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
 // We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
 FieldBuilder leftExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 leftExpression.addArgument(2);
 leftExpression.addArgument("+");
 leftExpression.addArgument(3);

 FieldBuilder rightExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 rightExpression.addArgument(2.5);
 rightExpression.addArgument("*");
 rightExpression.addArgument(5.2);

 // Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
 // These arguments will reuse the output values of our numeric expressions.
 FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
 trueOutput.addText("True, both expressions amount to ");
 trueOutput.addField(leftExpression);

 FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
 falseOutput.addNode(new Run(doc, "False, "));
 falseOutput.addField(leftExpression);
 falseOutput.addNode(new Run(doc, " does not equal "));
 falseOutput.addField(rightExpression);

 // Finally, we will create one more field builder for the IF field and combine all of the expressions.
 builder = new FieldBuilder(FieldType.FIELD_IF);
 builder.addArgument(leftExpression);
 builder.addArgument("=");
 builder.addArgument(rightExpression);
 builder.addArgument(trueOutput);
 builder.addArgument(falseOutput);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 Assert.assertEquals(" IF  = 2 + 3  =  = 2.5 * 5.2  " +
         "\"True, both expressions amount to  = 2 + 3 \" " +
         "\"False,  = 2 + 3  does not equal  = 2.5 * 5.2 \" ", field.getFieldCode());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SYMBOL.docx");
 
```

### addField(FieldBuilder fieldBuilder) {#addField-com.aspose.words.FieldBuilder}
```
public FieldArgumentBuilder addField(FieldBuilder fieldBuilder)
```


Adds a field represented by a [FieldBuilder](../../com.aspose.words/fieldbuilder/) to the argument.

 **Examples:** 

Shows how to construct fields using a field builder, and then insert them into the document.

```

 Document doc = new Document();

 // Below are three examples of field construction done using a field builder.
 // 1 -  Single field:
 // Use a field builder to add a SYMBOL field which displays the \u0192 (Florin) symbol.
 FieldBuilder builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(402);
 builder.addSwitch("\\f", "Arial");
 builder.addSwitch("\\s", 25);
 builder.addSwitch("\\u");
 Field field = builder.buildAndInsert(doc.getFirstSection().getBody().getFirstParagraph());

 Assert.assertEquals(field.getFieldCode(), " SYMBOL 402 \\f Arial \\s 25 \\u ");

 // 2 -  Nested field:
 // Use a field builder to create a formula field used as an inner field by another field builder.
 FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FIELD_FORMULA);
 innerFormulaBuilder.addArgument(100);
 innerFormulaBuilder.addArgument("+");
 innerFormulaBuilder.addArgument(74);

 // Create another builder for another SYMBOL field, and insert the formula field
 // that we have created above into the SYMBOL field as its argument.
 builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(innerFormulaBuilder);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 // The outer SYMBOL field will use the formula field result, 174, as its argument,
 // which will make the field display the ® (Registered Sign) symbol since its character number is 174.
 Assert.assertEquals(" SYMBOL  = 100 + 74  ", field.getFieldCode());

 // 3 -  Multiple nested fields and arguments:
 // Now, we will use a builder to create an IF field, which displays one of two custom string values,
 // depending on the true/false value of its expression. To get a true/false value
 // that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
 // We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
 FieldBuilder leftExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 leftExpression.addArgument(2);
 leftExpression.addArgument("+");
 leftExpression.addArgument(3);

 FieldBuilder rightExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 rightExpression.addArgument(2.5);
 rightExpression.addArgument("*");
 rightExpression.addArgument(5.2);

 // Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
 // These arguments will reuse the output values of our numeric expressions.
 FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
 trueOutput.addText("True, both expressions amount to ");
 trueOutput.addField(leftExpression);

 FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
 falseOutput.addNode(new Run(doc, "False, "));
 falseOutput.addField(leftExpression);
 falseOutput.addNode(new Run(doc, " does not equal "));
 falseOutput.addField(rightExpression);

 // Finally, we will create one more field builder for the IF field and combine all of the expressions.
 builder = new FieldBuilder(FieldType.FIELD_IF);
 builder.addArgument(leftExpression);
 builder.addArgument("=");
 builder.addArgument(rightExpression);
 builder.addArgument(trueOutput);
 builder.addArgument(falseOutput);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 Assert.assertEquals(" IF  = 2 + 3  =  = 2.5 * 5.2  " +
         "\"True, both expressions amount to  = 2 + 3 \" " +
         "\"False,  = 2 + 3  does not equal  = 2.5 * 5.2 \" ", field.getFieldCode());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SYMBOL.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldBuilder | [FieldBuilder](../../com.aspose.words/fieldbuilder/) |  |

**Returns:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/)
### addNode(Inline node) {#addNode-com.aspose.words.Inline}
```
public FieldArgumentBuilder addNode(Inline node)
```


Adds a node to the argument.

 **Remarks:** 

Only text level nodes are supported at the moment.

 **Examples:** 

Shows how to construct fields using a field builder, and then insert them into the document.

```

 Document doc = new Document();

 // Below are three examples of field construction done using a field builder.
 // 1 -  Single field:
 // Use a field builder to add a SYMBOL field which displays the \u0192 (Florin) symbol.
 FieldBuilder builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(402);
 builder.addSwitch("\\f", "Arial");
 builder.addSwitch("\\s", 25);
 builder.addSwitch("\\u");
 Field field = builder.buildAndInsert(doc.getFirstSection().getBody().getFirstParagraph());

 Assert.assertEquals(field.getFieldCode(), " SYMBOL 402 \\f Arial \\s 25 \\u ");

 // 2 -  Nested field:
 // Use a field builder to create a formula field used as an inner field by another field builder.
 FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FIELD_FORMULA);
 innerFormulaBuilder.addArgument(100);
 innerFormulaBuilder.addArgument("+");
 innerFormulaBuilder.addArgument(74);

 // Create another builder for another SYMBOL field, and insert the formula field
 // that we have created above into the SYMBOL field as its argument.
 builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(innerFormulaBuilder);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 // The outer SYMBOL field will use the formula field result, 174, as its argument,
 // which will make the field display the ® (Registered Sign) symbol since its character number is 174.
 Assert.assertEquals(" SYMBOL  = 100 + 74  ", field.getFieldCode());

 // 3 -  Multiple nested fields and arguments:
 // Now, we will use a builder to create an IF field, which displays one of two custom string values,
 // depending on the true/false value of its expression. To get a true/false value
 // that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
 // We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
 FieldBuilder leftExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 leftExpression.addArgument(2);
 leftExpression.addArgument("+");
 leftExpression.addArgument(3);

 FieldBuilder rightExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 rightExpression.addArgument(2.5);
 rightExpression.addArgument("*");
 rightExpression.addArgument(5.2);

 // Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
 // These arguments will reuse the output values of our numeric expressions.
 FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
 trueOutput.addText("True, both expressions amount to ");
 trueOutput.addField(leftExpression);

 FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
 falseOutput.addNode(new Run(doc, "False, "));
 falseOutput.addField(leftExpression);
 falseOutput.addNode(new Run(doc, " does not equal "));
 falseOutput.addField(rightExpression);

 // Finally, we will create one more field builder for the IF field and combine all of the expressions.
 builder = new FieldBuilder(FieldType.FIELD_IF);
 builder.addArgument(leftExpression);
 builder.addArgument("=");
 builder.addArgument(rightExpression);
 builder.addArgument(trueOutput);
 builder.addArgument(falseOutput);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 Assert.assertEquals(" IF  = 2 + 3  =  = 2.5 * 5.2  " +
         "\"True, both expressions amount to  = 2 + 3 \" " +
         "\"False,  = 2 + 3  does not equal  = 2.5 * 5.2 \" ", field.getFieldCode());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SYMBOL.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Inline](../../com.aspose.words/inline/) |  |

**Returns:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/)
### addText(String text) {#addText-java.lang.String}
```
public FieldArgumentBuilder addText(String text)
```


Adds a plain text to the argument.

 **Examples:** 

Shows how to construct fields using a field builder, and then insert them into the document.

```

 Document doc = new Document();

 // Below are three examples of field construction done using a field builder.
 // 1 -  Single field:
 // Use a field builder to add a SYMBOL field which displays the \u0192 (Florin) symbol.
 FieldBuilder builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(402);
 builder.addSwitch("\\f", "Arial");
 builder.addSwitch("\\s", 25);
 builder.addSwitch("\\u");
 Field field = builder.buildAndInsert(doc.getFirstSection().getBody().getFirstParagraph());

 Assert.assertEquals(field.getFieldCode(), " SYMBOL 402 \\f Arial \\s 25 \\u ");

 // 2 -  Nested field:
 // Use a field builder to create a formula field used as an inner field by another field builder.
 FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FIELD_FORMULA);
 innerFormulaBuilder.addArgument(100);
 innerFormulaBuilder.addArgument("+");
 innerFormulaBuilder.addArgument(74);

 // Create another builder for another SYMBOL field, and insert the formula field
 // that we have created above into the SYMBOL field as its argument.
 builder = new FieldBuilder(FieldType.FIELD_SYMBOL);
 builder.addArgument(innerFormulaBuilder);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 // The outer SYMBOL field will use the formula field result, 174, as its argument,
 // which will make the field display the ® (Registered Sign) symbol since its character number is 174.
 Assert.assertEquals(" SYMBOL  = 100 + 74  ", field.getFieldCode());

 // 3 -  Multiple nested fields and arguments:
 // Now, we will use a builder to create an IF field, which displays one of two custom string values,
 // depending on the true/false value of its expression. To get a true/false value
 // that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
 // We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
 FieldBuilder leftExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 leftExpression.addArgument(2);
 leftExpression.addArgument("+");
 leftExpression.addArgument(3);

 FieldBuilder rightExpression = new FieldBuilder(FieldType.FIELD_FORMULA);
 rightExpression.addArgument(2.5);
 rightExpression.addArgument("*");
 rightExpression.addArgument(5.2);

 // Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
 // These arguments will reuse the output values of our numeric expressions.
 FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
 trueOutput.addText("True, both expressions amount to ");
 trueOutput.addField(leftExpression);

 FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
 falseOutput.addNode(new Run(doc, "False, "));
 falseOutput.addField(leftExpression);
 falseOutput.addNode(new Run(doc, " does not equal "));
 falseOutput.addField(rightExpression);

 // Finally, we will create one more field builder for the IF field and combine all of the expressions.
 builder = new FieldBuilder(FieldType.FIELD_IF);
 builder.addArgument(leftExpression);
 builder.addArgument("=");
 builder.addArgument(rightExpression);
 builder.addArgument(trueOutput);
 builder.addArgument(falseOutput);
 field = builder.buildAndInsert(doc.getFirstSection().getBody().appendParagraph(""));

 Assert.assertEquals(" IF  = 2 + 3  =  = 2.5 * 5.2  " +
         "\"True, both expressions amount to  = 2 + 3 \" " +
         "\"False,  = 2 + 3  does not equal  = 2.5 * 5.2 \" ", field.getFieldCode());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SYMBOL.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String |  |

**Returns:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/)
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder/) |  |

