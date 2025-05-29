---
title: TextWatermarkOptions.FontSize
linktitle: FontSize
articleTitle: FontSize
second_title: Aspose.Words pour .NET
description: Personnalisez vos options de filigrane de texte grâce à la taille de police ajustable. Définissez facilement la taille souhaitée pour une visibilité et un style optimaux dans vos créations.
type: docs
weight: 40
url: /fr/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

Récupère ou définit la taille de police. La valeur par défaut est 0 (automatique).

```csharp
public float FontSize { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancé lorsque l'argument est hors de la plage de valeurs valides. |

## Remarques

Les valeurs valides vont de 0 à 65,5 inclus.

La taille de police automatique signifie que le filigrane sera mis à l'échelle à sa largeur maximale et à sa hauteur maximale par rapport aux marges de la page.

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

* class [TextWatermarkOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
