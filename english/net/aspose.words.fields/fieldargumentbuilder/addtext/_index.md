---
title: FieldArgumentBuilder.AddText
linktitle: AddText
articleTitle: AddText
second_title: Aspose.Words for .NET
description: Enhance your arguments with the FieldArgumentBuilder AddText method. Effortlessly add plain text for improved clarity and functionality.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldargumentbuilder/addtext/
---
## FieldArgumentBuilder.AddText method

Adds a plain text to the argument.

```csharp
public FieldArgumentBuilder AddText(string text)
```

## Examples

Shows how to construct fields using a field builder, and then insert them into the document.

```csharp
Document doc = new Document();

// Below are three examples of field construction done using a field builder.
// 1 -  Single field:
// Use a field builder to add a SYMBOL field which displays the ƒ (Florin) symbol.
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.That(field.GetFieldCode(), Is.EqualTo(" SYMBOL 402 \\f Arial \\s 25 \\u "));

// 2 -  Nested field:
// Use a field builder to create a formula field used as an inner field by another field builder.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Create another builder for another SYMBOL field, and insert the formula field
// that we have created above into the SYMBOL field as its argument. 
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// The outer SYMBOL field will use the formula field result, 174, as its argument,
// which will make the field display the ® (Registered Sign) symbol since its character number is 174.
Assert.That(field.GetFieldCode(), Is.EqualTo(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 "));

// 3 -  Multiple nested fields and arguments:
// Now, we will use a builder to create an IF field, which displays one of two custom string values,
// depending on the true/false value of its expression. To get a true/false value
// that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
// We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
// These arguments will reuse the output values of our numeric expressions.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

// Finally, we will create one more field builder for the IF field and combine all of the expressions. 
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.That(field.GetFieldCode(), Is.EqualTo(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" "));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### See Also

* class [FieldArgumentBuilder](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
