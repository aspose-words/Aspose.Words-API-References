---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words for .NET
description: Enhance your documents with the DocumentBuilder InsertStyleSeparator method, effortlessly adding style separators for improved formatting and organization.
type: docs
weight: 490
url: /net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Inserts style separator into the document.

```csharp
public void InsertStyleSeparator()
```

## Remarks

This method allows to apply different paragraph styles to two different parts of a text line.

## Examples

Shows how to work with style separators.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Each paragraph can only have one style.
// The InsertStyleSeparator method allows us to work around this limitation.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// Calling the InsertStyleSeparator method creates another paragraph,
// which can have a different style to the previous. There will be no break between paragraphs.
// The text in the output document will look like one paragraph with two styles.
Assert.That(doc.FirstSection.Body.Paragraphs.Count, Is.EqualTo(2));
Assert.That(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name, Is.EqualTo("Heading 1"));
Assert.That(doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name, Is.EqualTo("MyParaStyle"));

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
