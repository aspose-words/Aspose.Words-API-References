---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words for .NET
description: Discover how the Aspose.Words.Drawing.WrapType enum enhances text wrapping around shapes and images for professional document formatting.
type: docs
weight: 1810
url: /net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Specifies how text is wrapped around a shape or picture.

```csharp
public enum WrapType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `3` | No text wrapping around the shape. The shape is placed behind or in front of text. |
| Inline | `0` | The shape remains on the same layer as text and treated as a character. |
| TopBottom | `1` | The text stops at the top of the shape and restarts on the line below the shape. |
| Square | `2` | Wraps text around all sides of the square bounding box of the shape. |
| Tight | `4` | Wraps tightly around the edges of the shape, instead of wrapping around the bounding box. |
| Through | `5` | Same as Tight, but wraps inside any parts of the shape that are open. |

## Examples

Shows how to insert a floating image to the center of a page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Shows how to insert an image, and use it as a watermark.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert the image into the header so that it will be visible on every page.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Place the image at the center of the page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### See Also

* property [WrapType](../shapebase/wraptype/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
