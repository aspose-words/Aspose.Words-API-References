---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words pour .NET
description: Watermark SetText méthode. Ajoute un filigrane de texte dans le document en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

Ajoute un filigrane de texte dans le document.

```csharp
public void SetText(string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| text | String | Texte affiché sous forme de filigrane. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lance lorsque la longueur du texte est hors plage ou que le texte ne contient que des espaces. |
| ArgumentNullException | Lance lorsque le texte est`nul` . |

## Remarques

La longueur du texte doit être comprise entre 1 et 200 inclus. Le texte ne peut pas être`nul` ou ne contiennent que des espaces.

## Exemples

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

* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

Ajoute un filigrane de texte dans le document.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| text | String | Texte affiché sous forme de filigrane. |
| options | TextWatermarkOptions | Définit des options supplémentaires pour le filigrane de texte. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lance lorsque la longueur du texte est hors plage ou que le texte ne contient que des espaces. |
| ArgumentNullException | Lance lorsque le texte est`nul` . |

## Remarques

La longueur du texte doit être comprise entre 1 et 200 inclus. Le texte ne peut pas être`nul` ou ne contiennent que des espaces.

Si[`TextWatermarkOptions`](../../textwatermarkoptions/) est`nul`, le filigrane sera défini avec les options par défaut.

## Exemples

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
