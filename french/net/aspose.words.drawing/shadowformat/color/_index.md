---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Couleur ShadowFormat pour personnaliser les couleurs des ombres dans vos créations. La couleur par défaut est le noir, mais laissez libre cours à votre créativité avec des options éclatantes !
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Obtient unColor objet qui représente la couleur de l'ombre. La valeur par défaut estBlack .

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
