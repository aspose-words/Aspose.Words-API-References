---
title: DocumentBuilder.PushFont
linktitle: PushFont
articleTitle: PushFont
second_title: Aspose.Words for .NET
description: Discover how the DocumentBuilder PushFont method enhances your document formatting by saving character styles for easy retrieval and consistent design.
type: docs
weight: 640
url: /net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Saves current character formatting onto the stack.

```csharp
public void PushFont()
```

## Examples

Shows how to use a document builder's formatting stack.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set up font formatting, then write the text that goes before the hyperlink.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Preserve our current formatting configuration on the stack.
builder.PushFont();

// Alter the builder's current formatting by applying a new style.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.That(builder.Font.Color.ToArgb(), Is.EqualTo(Color.Blue.ToArgb()));
Assert.That(builder.Font.Underline, Is.EqualTo(Underline.Single));

// Restore the font formatting that we saved earlier and remove the element from the stack.
builder.PopFont();

Assert.That(builder.Font.Color.ToArgb(), Is.EqualTo(Color.Empty.ToArgb()));
Assert.That(builder.Font.Underline, Is.EqualTo(Underline.None));

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### See Also

* property [Font](../font/)
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
