---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words for .NET
description: PageSetup TextOrientation property. Allows to specify TextOrientation for the whole page. Default value is Horizontal in C#.
type: docs
weight: 430
url: /net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Allows to specify `TextOrientation` for the whole page. Default value is Horizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Remarks

This property is only supported for MS Word native formats DOCX, WML, RTF and DOC.

## Examples

Shows how to set text orientation.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
// to the right so that all left-to-right text now goes top-to-bottom.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### See Also

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
