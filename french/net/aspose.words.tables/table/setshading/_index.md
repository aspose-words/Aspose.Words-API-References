---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words pour .NET
description: Améliorez l'apparence de votre tableau avec la méthode SetShading, vous permettant d'appliquer des valeurs d'ombrage personnalisées pour un aspect soigné et professionnel.
type: docs
weight: 450
url: /fr/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Définit l'ombrage sur les valeurs spécifiées sur l'ensemble du tableau.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| texture | TextureIndex | La texture à appliquer. |
| foregroundColor | Color | La couleur de la texture. |
| backgroundColor | Color | La couleur du remplissage d'arrière-plan. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
