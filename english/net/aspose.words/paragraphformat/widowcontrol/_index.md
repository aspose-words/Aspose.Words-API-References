---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words for .NET
description: Discover how the ParagraphFormat WidowControl property ensures your text's first and last lines stay together on the same page for better readability.
type: docs
weight: 410
url: /net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.

```csharp
public bool WidowControl { get; set; }
```

## Examples

Shows how to enable widow/orphan control for a paragraph.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// When we write the text that does not fit onto one page, one line may spill over onto the next page.
// The single line that ends up on the next page is called an "Orphan",
// and the previous line where the orphan broke off is called a "Widow".
// We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
// If we wish to preserve our document's dimensions, we can set this flag to "true"
// to push widows onto the same page as their respective orphans. 
// Leave this flag as "false" will leave widow/orphan pairs in text.
// Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
// (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
builder.ParagraphFormat.WidowControl = widowControl; 

// Insert text that produces an orphan and a widow.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
