---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.TextWatermarkOptions pour des filigranes de texte personnalisables. Améliorez vos documents avec des options de personnalisation uniques et professionnelles !
type: docs
weight: 7290
url: /fr/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Contient des options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec du texte.

Pour en savoir plus, visitez le[Travailler avec le filigrane](https://docs.aspose.com/words/net/working-with-watermark/) article de documentation.

```csharp
public class TextWatermarkOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Obtient ou définit la couleur de police. La valeur par défaut estSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Récupère ou définit le nom de la famille de polices. La valeur par défaut est « Calibri ». |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Récupère ou définit la taille de police. La valeur par défaut est 0 (automatique). |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Obtient ou définit une valeur booléenne qui est responsable de l'opacité du filigrane. La valeur par défaut est`vrai` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Obtient ou définit la disposition du filigrane. La valeur par défaut estDiagonal . |

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
