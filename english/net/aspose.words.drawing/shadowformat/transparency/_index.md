---
title: ShadowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words for .NET
description: ShadowFormat.Transparency property sets shadow effect transparency from 0 opaque to 1 clear in Aspose.Words documents.
type: docs
weight: 20
url: /net/aspose.words.drawing/shadowformat/transparency/
---
## ShadowFormat.Transparency property

Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0.

```csharp
public double Transparency { get; set; }
```

## Examples

Shows how to set a color with transparency.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ShadowFormat shadowFormat = shape.ShadowFormat;
shadowFormat.Type = ShadowType.Shadow21;
shadowFormat.Color = Color.Red;
shadowFormat.Transparency = 0.8;

doc.Save(ArtifactsDir + "Shape.ShadowFormatTransparency.docx");
```

### See Also

* class [ShadowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
