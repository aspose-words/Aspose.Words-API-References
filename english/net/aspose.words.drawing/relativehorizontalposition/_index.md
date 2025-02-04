---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.RelativeHorizontalPosition enum. Specifies to what the horizontal position of a shape or text frame is relative in C#.
type: docs
weight: 1570
url: /net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Specifies to what the horizontal position of a shape or text frame is relative.

```csharp
public enum RelativeHorizontalPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Margin | `0` | Specifies that the horizontal positioning shall be relative to the page margins. |
| Page | `1` | The object is positioned relative to the left edge of the page. |
| Column | `2` | The object is positioned relative to the left side of the column. |
| Character | `3` | The object is positioned relative to the left side of the paragraph. |
| LeftMargin | `4` | Specifies that the horizontal positioning shall be relative to the left margin of the page. |
| RightMargin | `5` | Specifies that the horizontal positioning shall be relative to the right margin of the page. |
| InsideMargin | `6` | Specifies that the horizontal positioning shall be relative to the inside margin of the current page (the left margin on odd pages, right on even pages). |
| OutsideMargin | `7` | Specifies that the horizontal positioning shall be relative to the outside margin of the current page (the right margin on odd pages, left on even pages). |
| Default | `2` | Default value is Column. |

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

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
