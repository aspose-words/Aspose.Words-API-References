---
title: Table.SetShading
second_title: Référence de l'API Aspose.Words pour .NET
description: Table méthode. Définit lombrage sur les valeurs spécifiées sur toute la table.
type: docs
weight: 450
url: /fr/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Définit l'ombrage sur les valeurs spécifiées sur toute la table.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| texture | TextureIndex | La texture à appliquer. |
| foregroundColor | Color | La couleur de la texture. |
| backgroundColor | Color | La couleur du remplissage d'arrière-plan. |

### Exemples

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


