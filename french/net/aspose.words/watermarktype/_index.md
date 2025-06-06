---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.WatermarkType pour personnaliser facilement vos filigranes dans vos documents. Améliorez vos projets grâce à des options de filigrane polyvalentes !
type: docs
weight: 7540
url: /fr/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Spécifie le type de filigrane.

```csharp
public enum WatermarkType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Text | `0` | Indique que le texte sera utilisé comme filigrane. |
| Image | `1` | Indique que l'image sera utilisée comme filigrane. |
| None | `2` | Indique que le filigrane n'est pas défini. |

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
