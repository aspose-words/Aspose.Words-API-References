---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words for .NET
description: Discover the ShapeBase ScreenTip property, enhance user experience by customizing tooltip text that appears on mouse hover over shapes.
type: docs
weight: 510
url: /net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Defines the text displayed when the mouse pointer moves over the shape.

```csharp
public string ScreenTip { get; set; }
```

## Remarks

The default value is an empty string.

## Examples

Shows how to insert a shape which contains an image, and is also a hyperlink.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
// and take us to the hyperlink in the "HRef" property.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
