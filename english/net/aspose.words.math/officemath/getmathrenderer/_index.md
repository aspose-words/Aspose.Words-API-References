---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words for .NET
description: Discover OfficeMath's GetMathRenderer method to effortlessly convert equations into images, enhancing your documents with clear, professional visuals.
type: docs
weight: 90
url: /net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Creates and returns an object that can be used to render this equation into an image.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Return Value

The renderer object for this equation.

## Remarks

This method just invokes the [`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) constructor and passes this object as a parameter.

## Examples

Shows how to render an Office Math object into an image file in the local file system.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
// how it renders the OfficeMath node into an image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Set the "Scale" property to 5 to render the object to five times its original size.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### See Also

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* namespace [Aspose.Words.Math](../../../aspose.words.math/)
* assembly [Aspose.Words](../../../)
