---
title: DocumentBuilder.PopFont
linktitle: PopFont
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder PopFont method. Retrieves character formatting previously saved on the stack in C#.
type: docs
weight: 590
url: /net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Retrieves character formatting previously saved on the stack.

```csharp
public void PopFont()
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

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Restore the font formatting that we saved earlier and remove the element from the stack.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### See Also

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
