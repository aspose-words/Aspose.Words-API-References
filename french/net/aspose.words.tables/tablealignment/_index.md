---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Tables.TableAlignment pour un alignement optimal des tableaux en ligne. Améliorez la mise en forme de vos documents avec précision et simplicité.
type: docs
weight: 7200
url: /fr/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Spécifie l'alignement d'un tableau en ligne.

```csharp
public enum TableAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Left | `0` | Le tableau est aligné à gauche. |
| Center | `1` | Le tableau est centré. |
| Right | `2` | Le tableau est aligné à droite. |

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

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
