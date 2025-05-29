---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Watermark pour ajouter et personnaliser facilement des filigranes dans vos documents, améliorant ainsi le professionnalisme et l'image de marque.
type: docs
weight: 7520
url: /fr/net/aspose.words/watermark/
---
## Watermark class

Représente la classe avec laquelle travailler le filigrane du document.

Pour en savoir plus, visitez le[Travailler avec le filigrane](https://docs.aspose.com/words/net/working-with-watermark/) article de documentation.

```csharp
public sealed class Watermark
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Obtient le type de filigrane. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Supprime le filigrane. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Ajoute un filigrane d'image dans le document. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Ajoute un filigrane d'image dans le document. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Ajoute un filigrane d'image dans le document. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Ajoute un filigrane d'image dans le document. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Ajoute un filigrane de texte dans le document. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Ajoute un filigrane de texte dans le document. |

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
