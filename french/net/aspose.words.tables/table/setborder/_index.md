---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words pour .NET
description: Table SetBorder méthode. Définit la bordure du tableau spécifiée sur le style de ligne la largeur et la couleur spécifiés en C#.
type: docs
weight: 410
url: /fr/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Définit la bordure du tableau spécifiée sur le style de ligne, la largeur et la couleur spécifiés.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| borderType | BorderType | La bordure du tableau à changer. |
| lineStyle | LineStyle | Le style de ligne à appliquer. |
| lineWidth | Double | La largeur de ligne à définir (en points). |
| color | Color | La couleur à utiliser pour la bordure. |
| isOverrideCellBorders | Boolean | Quand`vrai`, entraîne la suppression de toutes les bordures de cellules explicites existantes. |

## Exemples

Montre comment appliquer une bordure de contour à un tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Aligne le tableau au centre de la page.
table.Alignment = TableAlignment.Center;

// Supprime toutes les bordures et tous les ombrages existants du tableau.
table.ClearBorders();
table.ClearShading();

// Ajoute des bordures vertes au contour du tableau.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Remplit les cellules avec une couleur unie vert clair.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Voir également

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
