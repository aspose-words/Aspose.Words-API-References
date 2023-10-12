---
title: ShapeBase.IsTopLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Retoursvraisi cette forme nest pas un enfant dune forme de groupe.
type: docs
weight: 350
url: /fr/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Retours`vrai`si cette forme n'est pas un enfant d'une forme de groupe.

```csharp
public bool IsTopLevel { get; }
```

### Exemples

Montre comment savoir si une forme fait partie d’une forme de groupe.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Par défaut, une forme ne fait partie d'aucune forme de groupe et sa propriété "IsTopLevel" est donc définie sur "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Une fois que l'on assimile une forme à une forme de groupe, la propriété "IsTopLevel" passe à "false".
Assert.False(shape.IsTopLevel);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


