---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Alignement des tableaux pour contrôler sans effort le positionnement des tableaux en ligne dans vos documents pour un aspect soigné et professionnel.
type: docs
weight: 40
url: /fr/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Spécifie comment un tableau en ligne est aligné dans le document.

```csharp
public TableAlignment Alignment { get; set; }
```

## Remarques

La valeur par défaut estLeft.

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

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
