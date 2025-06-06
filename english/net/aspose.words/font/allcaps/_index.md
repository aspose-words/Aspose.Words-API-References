---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: Aspose.Words for .NET
description: Discover the Font AllCaps property. Easily format text in all capital letters for enhanced readability and impactful design in your projects.
type: docs
weight: 10
url: /net/aspose.words/font/allcaps/
---
## Font.AllCaps property

True if the font is formatted as all capital letters.

```csharp
public bool AllCaps { get; set; }
```

## Examples

Shows how to format a run to display its contents in capitals.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
// 1 -  Set the AllCaps flag to display all characters in regular capitals:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 -  Set the SmallCaps flag to display all characters in small capitals:
// If a character is lower case, it will appear in its upper case form
// but will have the same height as the lower case (the font's x-height).
// Characters that were in upper case originally will look the same.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
