---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words for .NET
description: ShapeBase HRef property. Gets or sets the full hyperlink address for a shape in C#.
type: docs
weight: 230
url: /net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Gets or sets the full hyperlink address for a shape.

```csharp
public string HRef { get; set; }
```

## Remarks

The default value is an empty string.

Below are examples of valid values for this property:

Full URI: `https://www.aspose.com/`.

Full file name: `C:\\My Documents\\SalesReport.doc`.

Relative URI: `../../../resource.txt`

Relative file name: `..\\My Documents\\SalesReport.doc`.

Bookmark within another document: `https://www.aspose.com/Products/Default.aspx#Suites`

Bookmark within this document: `#BookmakName`.

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
