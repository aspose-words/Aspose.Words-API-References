---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.WatermarkLayout pour un positionnement optimal des filigranes. Améliorez la conception de vos documents grâce à un contrôle précis de la mise en page et à une personnalisation.
type: docs
weight: 7530
url: /fr/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Définit la disposition du filigrane par rapport au centre du filigrane.

```csharp
public enum WatermarkLayout
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Horizontal | `0` | Disposition horizontale du filigrane. Correspond à une rotation de 0 degré. |
| Diagonal | `315` | Disposition du filigrane en diagonale. Correspond à une rotation de 315 degrés. |

## Exemples

Montre comment créer un filigrane de texte.

```csharp
Document doc = new Document();

// Ajouter un filigrane en texte brut.
doc.Watermark.SetText("Aspose Watermark");

// Si nous souhaitons modifier la mise en forme du texte en l'utilisant comme filigrane,
// nous pouvons le faire en passant un objet TextWatermarkOptions lors de la création du filigrane.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Nous pouvons supprimer un filigrane d'un document comme celui-ci.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
