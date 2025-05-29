---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words pour .NET
description: Découvrez ShapeBase IsTopLevel. Vérifiez rapidement si une forme est autonome et optimisez votre flux de travail de conception grâce à une gestion efficace des groupes.
type: docs
weight: 370
url: /fr/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Retours`vrai` si cette forme n'est pas un enfant d'une forme de groupe.

```csharp
public bool IsTopLevel { get; }
```

## Exemples

Montre comment déterminer si une forme fait partie d’un groupe de formes.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Une forme par défaut ne fait partie d'aucune forme de groupe et a donc la propriété « IsTopLevel » définie sur « true ».
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Une fois que nous assimilons une forme à une forme de groupe, la propriété « IsTopLevel » devient « false ».
Assert.False(shape.IsTopLevel);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
