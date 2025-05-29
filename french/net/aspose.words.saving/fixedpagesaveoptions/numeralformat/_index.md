---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FixedPageSaveOptions NumeralFormat pour personnaliser le rendu numérique. Passez facilement aux chiffres européens pour une présentation améliorée de vos documents.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Obtient ou définit[`NumeralFormat`](../../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Remarques

Si la valeur de cette propriété est modifiée et que la mise en page est déjà créée, alors [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) est invoqué automatiquement pour mettre à jour toutes les modifications.

## Exemples

Montre comment définir le format numérique utilisé lors de l'enregistrement au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « NumeralFormat » sur « NumeralFormat.ArabicIndic » pour
// utiliser les glyphes de la plage U+0660 à U+0669 comme nombres.
// Définissez la propriété « NumeralFormat » sur « NumeralFormat.Context » pour
// recherchez les paramètres régionaux pour déterminer le nombre de glyphes à utiliser.
// Définissez la propriété « NumeralFormat » sur « NumeralFormat.EasternArabicIndic » pour
// utiliser les glyphes de la plage U+06F0 à U+06F9 comme nombres.
// Définissez la propriété « NumeralFormat » sur « NumeralFormat.European » pour utiliser les chiffres européens.
// Définissez la propriété « NumeralFormat » sur « NumeralFormat.System » pour déterminer le jeu de symboles à partir des paramètres régionaux.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Voir également

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
