---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: Restore your text to its original style with the Font ClearFormatting method. Enjoy clean, consistent formatting for a polished look!
type: docs
weight: 560
url: /net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Resets to default font formatting.

```csharp
public void ClearFormatting()
```

## Remarks

Removes all font formatting specified explicitly on the object from which [`Font`](../) was obtained so the font formatting will be inherited from the appropriate parent.

## Examples

Shows how to insert a hyperlink field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insert a hyperlink and emphasize it with custom formatting.
// The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
