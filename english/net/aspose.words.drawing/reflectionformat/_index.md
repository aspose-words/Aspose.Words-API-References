---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Drawing.ReflectionFormat class for advanced object reflection formatting. Enhance your document design with seamless integration!
type: docs
weight: 1560
url: /net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Represents the reflection formatting for an object.

```csharp
public class ReflectionFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Gets or sets a double value that specifies the degree of blur effect applied to the reflection effect in points. The default value is 0.0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Gets or sets a double value that specifies the amount of separation of the reflected image from the object in points. The default value is 0.0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Gets or sets a double value between 0.0 and 1.0 representing the size of the reflection as a percentage of the reflected object. The default value is 0.0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Gets or sets a double value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency for the reflection effect. The default value is 0.0. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Removes `ReflectionFormat` from the parent object. |

## Remarks

Use the [`Reflection`](../shapebase/reflection/) property to access reflection properties of an object. You do not create instances of the `ReflectionFormat` class directly.

## Examples

Shows how to interact with reflection shape effect.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.That(reflectionFormat.Transparency, Is.EqualTo(0.37d).Within(0.01d));
Assert.That(reflectionFormat.Size, Is.EqualTo(0.48d).Within(0.01d));
Assert.That(reflectionFormat.Blur, Is.EqualTo(17.5d).Within(0.01d));
Assert.That(reflectionFormat.Distance, Is.EqualTo(9.2d).Within(0.01d));

reflectionFormat.Remove();

Assert.That(reflectionFormat.Transparency, Is.EqualTo(0));
Assert.That(reflectionFormat.Size, Is.EqualTo(0));
Assert.That(reflectionFormat.Blur, Is.EqualTo(0));
Assert.That(reflectionFormat.Distance, Is.EqualTo(0));
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
