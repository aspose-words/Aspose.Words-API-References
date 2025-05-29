---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase ShadowFormat pour sublimer vos créations avec des effets d'ombre personnalisables pour les formes. Améliorez votre attrait visuel dès aujourd'hui !
type: docs
weight: 520
url: /fr/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Obtient la mise en forme de l'ombre pour la forme.

```csharp
public ShadowFormat ShadowFormat { get; }
```

## Exemples

Montre comment obtenir la couleur de l'ombre.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Voir également

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
