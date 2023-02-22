---
title: Enum WatermarkLayout
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.WatermarkLayout énumération. Définit la disposition du filigrane par rapport au centre du filigrane.
type: docs
weight: 6370
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
| Horizontal | `0` | Disposition horizontale du filigrane. Correspond à 0 degré de rotation. |
| Diagonal | `315` | Disposition du filigrane en diagonale. Correspond à 315 degrés de rotation. |

### Exemples

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


