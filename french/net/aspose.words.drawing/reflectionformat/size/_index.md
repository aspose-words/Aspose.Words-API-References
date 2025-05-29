---
title: ReflectionFormat.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ReflectionFormat Size : contrôlez la taille de la réflexion (0,0-1,0) pour des effets visuels époustouflants dans vos créations. Améliorez l'esthétique de votre projet !
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/reflectionformat/size/
---
## ReflectionFormat.Size property

Obtient ou définit une valeur double entre 0,0 et 1,0 représentant la taille de la réflexion en pourcentage de l'objet réfléchi. La valeur par défaut est 0,0.

```csharp
public double Size { get; set; }
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

* class [ReflectionFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
