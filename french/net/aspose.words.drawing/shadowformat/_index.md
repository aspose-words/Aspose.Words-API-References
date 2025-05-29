---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Drawing.ShadowFormat pour des effets d'ombre améliorés. Améliorez la conception de vos documents grâce à des options de mise en forme d'ombre personnalisables.
type: docs
weight: 1620
url: /fr/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Représente la mise en forme de l'ombre pour un objet.

Pour en savoir plus, visitez le[Travailler avec des éléments graphiques](https://docs.aspose.com/words/net/working-with-graphic-elements/) article de documentation.

```csharp
public class ShadowFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Obtient unColor objet qui représente la couleur de l'ombre. La valeur par défaut estBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Obtient ou définit le spécifié[`ShadowType`](../shadowtype/) pour ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Retours`vrai` si la mise en forme appliquée à cette instance est visible. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Efface le format d'ombre. |

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

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
