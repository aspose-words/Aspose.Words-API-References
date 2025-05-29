---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.NumeralFormat pour une représentation numérique optimale dans les formats de page fixes. Améliorez le rendu de vos documents dès aujourd'hui !
type: docs
weight: 6090
url: /fr/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Indique le jeu de symboles utilisé pour représenter les nombres lors du rendu dans des formats de page fixes.

```csharp
public enum NumeralFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| European | `0` | Chiffres européens : 0123456789. |
| ArabicIndic | `1` | Chiffres utilisés en arabe : ٠١٢٣٤٥٦٧٨٩. Plage Unicode U+0660 - u+0669. |
| EasternArabicIndic | `2` | Chiffres utilisés en persan et en ourdou : ۰۱۲۳۴۵۶۷۸۹. Plage Unicode U+06F0 - u+06F9. |
| Context | `3` | L'ensemble de symboles est déterminé à partir du contexte (paramètres régionaux et propriété RTL). |
| System | `4` | CETTE OPTION N'EST PAS PRIS EN CHARGE. L'ensemble de symboles est déterminé à partir des paramètres régionaux. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
