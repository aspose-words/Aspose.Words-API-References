---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ReflectionFormat class. Represents the reflection formatting for an object in C#.
type: docs
weight: 1550
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

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
