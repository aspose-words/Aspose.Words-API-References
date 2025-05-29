---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Explorez la propriété Type ShadowFormat pour personnaliser facilement vos effets d'ombre. Obtenez ou définissez ShadowType pour une plus grande flexibilité de conception.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Obtient ou définit le spécifié[`ShadowType`](../../shadowtype/) pour ShadowFormat.

```csharp
public ShadowType Type { get; set; }
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

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
