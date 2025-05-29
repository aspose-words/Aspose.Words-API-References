---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.MeasurementUnits pour une sélection précise des unités lors du traitement de vos documents. Améliorez votre flux de travail grâce à des options de mesure précises !
type: docs
weight: 4840
url: /fr/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Spécifie l'unité de mesure.

```csharp
public enum MeasurementUnits
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Inches | `0` | Pouces. |
| Centimeters | `1` | Centimètres. |
| Millimeters | `2` | Millimètres. |
| Points | `3` | Points. |
| Picas | `4` | Picas (couramment utilisé dans l'espacement des polices de machines à écrire traditionnelles). |

## Exemples

Montre comment rendre un document enregistré conforme à un ancien schéma ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
