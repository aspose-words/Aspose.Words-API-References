---
title: TextWatermarkOptions.Color
second_title: Référence de l'API Aspose.Words pour .NET
description: TextWatermarkOptions propriété. Obtient ou définit la couleur de la police. La valeur par défaut estSilver .
type: docs
weight: 20
url: /fr/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Obtient ou définit la couleur de la police. La valeur par défaut estSilver .

```csharp
public Color Color { get; set; }
```

### Exemples

Montre comment créer un filigrane de texte.

```csharp
Document doc = new Document();

// Ajoute un filigrane en texte brut.
doc.Watermark.SetText("Aspose Watermark");

// Si l'on souhaite éditer la mise en forme du texte en l'utilisant comme filigrane,
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
* espace de noms [Aspose.Words](../../textwatermarkoptions/)
* Assemblée [Aspose.Words](../../../)


