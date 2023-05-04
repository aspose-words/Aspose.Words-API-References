---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.VerticalAlignment enum. Specifies vertical alignment of a floating shape text frame or a floating table in C#.
type: docs
weight: 1350
url: /net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Specifies vertical alignment of a floating shape, text frame or a floating table.

```csharp
public enum VerticalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | The object is explicitly positioned, usually using its **Top** property. |
| Top | `1` | Specifies that the object shall be at the top of the vertical alignment base. |
| Center | `2` | Specifies that the object shall be centered with respect to the vertical alignment base. |
| Bottom | `3` | Specifies that the object shall be at the bottom of the vertical alignment base. |
| Inside | `4` | Specifies that the object shall be inside of the horizontal alignment base. |
| Outside | `5` | Specifies that the object shall be outside of the vertical alignment base. |
| Inline | `-1` | Not documented. Seems to be a possible value for floating paragraphs and tables. |
| Default | `0` | Same as None. |

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

### See Also

* property [VerticalAlignment](../shapebase/verticalalignment/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
