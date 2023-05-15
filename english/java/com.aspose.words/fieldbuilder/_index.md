---
title: FieldBuilder
linktitle: FieldBuilder
second_title: Aspose.Words for Java
description: Builds a field from field code tokens arguments and switches in Java.
type: docs
weight: 177
url: /java/com.aspose.words/fieldbuilder/
---

**Inheritance:**
java.lang.Object
```
public class FieldBuilder
```

Builds a field from field code tokens (arguments and switches).

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
| [FieldBuilder(int fieldType)](#FieldBuilder-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [addArgument(FieldArgumentBuilder argument)](#addArgument-com.aspose.words.FieldArgumentBuilder) | Adds a field's argument represented by [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/) to the field's code. |
| [addArgument(FieldBuilder argument)](#addArgument-com.aspose.words.FieldBuilder) | Adds a child field represented by another [FieldBuilder](../../com.aspose.words/fieldbuilder/) to the field's code. |
| [addArgument(double argument)](#addArgument-double) | Adds a field's argument. |
| [addArgument(int argument)](#addArgument-int) | Adds a field's argument. |
| [addArgument(String argument)](#addArgument-java.lang.String) | Adds a field's argument. |
| [addSwitch(String switchName)](#addSwitch-java.lang.String) | Adds a field's switch. |
| [addSwitch(String switchName, double switchArgument)](#addSwitch-java.lang.String-double) | Adds a field's switch. |
| [addSwitch(String switchName, int switchArgument)](#addSwitch-java.lang.String-int) | Adds a field's switch. |
| [addSwitch(String switchName, String switchArgument)](#addSwitch-java.lang.String-java.lang.String) | Adds a field's switch. |
| [buildAndInsert(Inline refNode)](#buildAndInsert-com.aspose.words.Inline) | Builds and inserts a field into the document before the specified inline node. |
| [buildAndInsert(Paragraph refNode)](#buildAndInsert-com.aspose.words.Paragraph) | Builds and inserts a field into the document to the end of the specified paragraph. |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FieldBuilder(int fieldType) {#FieldBuilder-int}
```
public FieldBuilder(int fieldType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |

### addArgument(FieldArgumentBuilder argument) {#addArgument-com.aspose.words.FieldArgumentBuilder}
```
public FieldBuilder addArgument(FieldArgumentBuilder argument)
```


Adds a field's argument represented by [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/) to the field's code.

 **Remarks:** 

This overload is used when the argument consists of a mixture of different parts such as child fields, nodes, and plain text.

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
| argument | [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder/) |  |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addArgument(FieldBuilder argument) {#addArgument-com.aspose.words.FieldBuilder}
```
public FieldBuilder addArgument(FieldBuilder argument)
```


Adds a child field represented by another [FieldBuilder](../../com.aspose.words/fieldbuilder/) to the field's code.

 **Remarks:** 

This overload is used when the argument consists of a single child field.

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
| argument | [FieldBuilder](../../com.aspose.words/fieldbuilder/) |  |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addArgument(double argument) {#addArgument-double}
```
public FieldBuilder addArgument(double argument)
```


Adds a field's argument.

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
| argument | double | The argument value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addArgument(int argument) {#addArgument-int}
```
public FieldBuilder addArgument(int argument)
```


Adds a field's argument.

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
| argument | int | The argument value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addArgument(String argument) {#addArgument-java.lang.String}
```
public FieldBuilder addArgument(String argument)
```


Adds a field's argument.

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
| argument | java.lang.String | The argument value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addSwitch(String switchName) {#addSwitch-java.lang.String}
```
public FieldBuilder addSwitch(String switchName)
```


Adds a field's switch.

 **Remarks:** 

This overload adds a flag (switch without argument).

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
| switchName | java.lang.String | The switch name. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addSwitch(String switchName, double switchArgument) {#addSwitch-java.lang.String-double}
```
public FieldBuilder addSwitch(String switchName, double switchArgument)
```


Adds a field's switch.

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
| switchName | java.lang.String | The switch name. |
| switchArgument | double | The switch value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addSwitch(String switchName, int switchArgument) {#addSwitch-java.lang.String-int}
```
public FieldBuilder addSwitch(String switchName, int switchArgument)
```


Adds a field's switch.

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
| switchName | java.lang.String | The switch name. |
| switchArgument | int | The switch value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### addSwitch(String switchName, String switchArgument) {#addSwitch-java.lang.String-java.lang.String}
```
public FieldBuilder addSwitch(String switchName, String switchArgument)
```


Adds a field's switch.

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
| switchName | java.lang.String | The switch name. |
| switchArgument | java.lang.String | The switch value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder/)
### buildAndInsert(Inline refNode) {#buildAndInsert-com.aspose.words.Inline}
```
public Field buildAndInsert(Inline refNode)
```


Builds and inserts a field into the document before the specified inline node.

 **Examples:** 

Shows how to create and insert a field using a field builder.

```

 Document doc = new Document();

 // A convenient way of adding text content to a document is with a document builder.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write(" Hello world! This text is one Run, which is an inline node.");

 // Fields have their builder, which we can use to construct a field code piece by piece.
 // In this case, we will construct a BARCODE field representing a US postal code,
 // and then insert it in front of a Run.
 FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FIELD_BARCODE);
 fieldBuilder.addArgument("90210");
 fieldBuilder.addSwitch("\\f", "A");
 fieldBuilder.addSwitch("\\u");

 fieldBuilder.buildAndInsert(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0));

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.CreateWithFieldBuilder.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| refNode | [Inline](../../com.aspose.words/inline/) |  |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### buildAndInsert(Paragraph refNode) {#buildAndInsert-com.aspose.words.Paragraph}
```
public Field buildAndInsert(Paragraph refNode)
```


Builds and inserts a field into the document to the end of the specified paragraph.

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
| refNode | [Paragraph](../../com.aspose.words/paragraph/) |  |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder/) |  |

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

