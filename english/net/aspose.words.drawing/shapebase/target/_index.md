---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words for .NET
description: Discover ShapeBase Target property to easily set or retrieve hyperlink target frames for your shapes, enhancing user navigation and experience.
type: docs
weight: 560
url: /net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Gets or sets the target frame for the shape hyperlink.

```csharp
public string Target { get; set; }
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
