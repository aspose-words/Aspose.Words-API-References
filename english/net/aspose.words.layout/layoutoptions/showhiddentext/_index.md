---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words for .NET
description: LayoutOptions ShowHiddenText property. Gets or sets indication of whether hidden text in the document is rendered. Default is false in C#.
type: docs
weight: 80
url: /net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Gets or sets indication of whether hidden text in the document is rendered. Default is `false`.

```csharp
public bool ShowHiddenText { get; set; }
```

## Remarks

This property affects all hidden content, not just text.

## Examples

Shows how to hide text in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### See Also

* class [LayoutOptions](../)
* namespace [Aspose.Words.Layout](../../layoutoptions/)
* assembly [Aspose.Words](../../../)
