---
title: Table.ClearShading
linktitle: ClearShading
articleTitle: ClearShading
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Table ClearShading pour éliminer sans effort l'ombrage des tableaux, améliorant ainsi la clarté et la présentation de vos projets.
type: docs
weight: 400
url: /fr/net/aspose.words.tables/table/clearshading/
---
## Table.ClearShading method

Supprime tout l'ombrage sur le tableau.

```csharp
public void ClearShading()
```

## Exemples

Montre comment appliquer une bordure de contour à un tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Alignez le tableau au centre de la page.
table.Alignment = TableAlignment.Center;

// Supprimez toutes les bordures et tous les ombrages existants du tableau.
table.ClearBorders();
table.ClearShading();

// Ajoutez des bordures vertes au contour du tableau.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Remplissez les cellules avec une couleur unie vert clair.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
