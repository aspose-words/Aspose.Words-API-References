---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words for .NET
description: Discover ShapeBase MarkupLanguage property for enhanced graphic object management. Unlock seamless integration and improved design efficiency today!
type: docs
weight: 410
url: /net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Gets MarkupLanguage used for this graphic object.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

## Examples

Shows how to verify a shape's size and markup language.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.That(shape.MarkupLanguage, Is.EqualTo(ShapeMarkupLanguage.Dml));
Assert.That(shape.SizeInPoints, Is.EqualTo(new SizeF(300, 300)));
```

### See Also

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
