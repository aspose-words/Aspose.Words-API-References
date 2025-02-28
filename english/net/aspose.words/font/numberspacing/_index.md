---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words for .NET
description: Discover the Font NumberSpacing property to customize numeral spacing for enhanced readability and design. Optimize your typography today!
type: docs
weight: 290
url: /net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Gets or sets the spacing type of the numeral being displayed.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Examples

Shows how to set the spacing type of the numeral.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// This effect is only supported in newer versions of MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### See Also

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
