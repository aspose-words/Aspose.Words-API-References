---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words pour .NET
description: Contrôlez la visibilité des formes grâce à la propriété cachée de ShapeBase. Basculez facilement entre visible et masqué pour une plus grande flexibilité de conception.
type: docs
weight: 230
url: /fr/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Obtient ou définit une valeur booléenne indiquant si la forme est visible.

```csharp
public bool Hidden { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

## Exemples

Montre comment masquer la forme.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
