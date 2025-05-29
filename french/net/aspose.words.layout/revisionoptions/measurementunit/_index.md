---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words pour .NET
description: Personnalisez vos commentaires de révision avec la propriété MeasurementUnit de RevisionOptions. Définissez facilement les unités de mesure, avec les centimètres comme valeur par défaut.
type: docs
weight: 80
url: /fr/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Permet de spécifier les unités de mesure pour les commentaires de révision. La valeur par défaut estCentimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

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

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
