---
title: ParagraphFormat.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words for .NET
description: Adjust the left indent for your paragraphs effortlessly with the ParagraphFormat LeftIndent property. Customize your text layout for better readability!
type: docs
weight: 180
url: /net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

Gets or sets the value (in points) that represents the left indent for paragraph.

```csharp
public double LeftIndent { get; set; }
```

## Examples

Shows how to configure paragraph formatting to create off-center text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Center all text that the document builder writes, and set up indents.
// The indent configuration below will create a body of text that will sit asymmetrically on the page.
// The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
