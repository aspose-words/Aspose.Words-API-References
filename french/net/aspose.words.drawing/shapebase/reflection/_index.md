---
title: ShapeBase.Reflection
linktitle: Reflection
articleTitle: Reflection
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase Reflection pour améliorer vos conceptions avec un formatage de réflexion personnalisable pour des effets visuels époustouflants.
type: docs
weight: 440
url: /fr/net/aspose.words.drawing/shapebase/reflection/
---
## ShapeBase.Reflection property

Obtient le formatage de réflexion pour la forme.

```csharp
public ReflectionFormat Reflection { get; }
```

## Exemples

Montre comment interagir avec l'effet de forme de réflexion.

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

### Voir également

* class [ReflectionFormat](../../reflectionformat/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
