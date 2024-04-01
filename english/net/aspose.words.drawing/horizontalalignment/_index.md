---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.HorizontalAlignment enum. Specifies horizontal alignment of a floating shape text frame or floating table in C#.
type: docs
weight: 1140
url: /net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Specifies horizontal alignment of a floating shape, text frame or floating table.

```csharp
public enum HorizontalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | The object is explicitly positioned, usually using its **Left** property. |
| Default | `0` | Same as None. |
| Left | `1` | Specifies that the object shall be left aligned to the horizontal alignment base. |
| Center | `2` | Specifies that the object shall be centered with respect to the horizontal alignment base. |
| Right | `3` | Specifies that the object shall be right aligned to the horizontal alignment base. |
| Inside | `4` | Specifies that the object shall be inside of the horizontal alignment base. |
| Outside | `5` | Specifies that the object shall be outside of the horizontal alignment base. |

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

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
