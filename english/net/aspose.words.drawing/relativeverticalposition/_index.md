---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.RelativeVerticalPosition enum. Specifies to what the vertical position of a shape or text frame is relative in C#.
type: docs
weight: 1310
url: /net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Specifies to what the vertical position of a shape or text frame is relative.

```csharp
public enum RelativeVerticalPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Margin | `0` | Specifies that the vertical positioning shall be relative to the page margins. |
| Page | `1` | The object is positioned relative to the top edge of the page. |
| Paragraph | `2` | The object is positioned relative to the top of the paragraph that contains the anchor. |
| Line | `3` | Undocumented. |
| TopMargin | `4` | Specifies that the vertical positioning shall be relative to the top margin of the current page. |
| BottomMargin | `5` | Specifies that the vertical positioning shall be relative to the bottom margin of the current page. |
| InsideMargin | `6` | Specifies that the vertical positioning shall be relative to the inside margin of the current page. |
| OutsideMargin | `7` | Specifies that the vertical positioning shall be relative to the outside margin of the current page. |
| TableDefault | `0` | Default value is Margin. |
| TextFrameDefault | `2` | Default value is Paragraph. |

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

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
