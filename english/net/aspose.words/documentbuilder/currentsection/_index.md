---
title: DocumentBuilder.CurrentSection
linktitle: CurrentSection
articleTitle: CurrentSection
second_title: Aspose.Words for .NET
description: Discover the DocumentBuilder CurrentSection property to easily access and manage the selected section in your document, enhancing your editing experience.
type: docs
weight: 60
url: /net/aspose.words/documentbuilder/currentsection/
---
## DocumentBuilder.CurrentSection property

Gets the section that is currently selected in this [`DocumentBuilder`](../).

```csharp
public Section CurrentSection { get; }
```

## Examples

Shows how to insert a floating image, and specify its position and size.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
// as the shape's horizontal distance, in points, from the left side of the page. 
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Set the shape's horizontal distance from the left side of the page to 100.
shape.Left = 100;

// Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Set the shape's height, which will automatically scale the width to preserve dimensions.
shape.Height = 125;

Assert.That(shape.Width, Is.EqualTo(125.0d));

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
Assert.That(shape.Bottom, Is.EqualTo(shape.Top + shape.Height));
Assert.That(shape.Right, Is.EqualTo(shape.Left + shape.Width));

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### See Also

* class [Section](../../section/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
