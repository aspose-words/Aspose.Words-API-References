---
title: FindReplaceOptions.ApplyParagraphFormat
linktitle: ApplyParagraphFormat
articleTitle: ApplyParagraphFormat
second_title: Aspose.Words for .NET
description: Discover the ApplyParagraphFormat property in FindReplaceOptions for seamless paragraph formatting in your documents. Enhance your content effortlessly!
type: docs
weight: 30
url: /net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Paragraph formatting applied to new content.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

## Examples

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.That(paragraphs[0].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));
Assert.That(paragraphs[1].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));
Assert.That(paragraphs[2].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// that contains a match that the find-and-replace operation finds.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Replace every full stop that is right before a paragraph break with an exclamation point.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.That(count, Is.EqualTo(2));
Assert.That(paragraphs[0].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));
Assert.That(paragraphs[1].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));
Assert.That(paragraphs[2].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!"));
```

### See Also

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
