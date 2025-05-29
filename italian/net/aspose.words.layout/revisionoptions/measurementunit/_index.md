---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words per .NET
description: Personalizza i commenti di revisione con la proprietà MeasurementUnit di RevisionOptions. Imposta facilmente le unità di misura, impostando i centimetri come predefinita.
type: docs
weight: 80
url: /it/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Consente di specificare le unità di misura per i commenti di revisione. Il valore predefinito èCentimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

## Esempi

Mostra come rendere un documento salvato conforme a uno schema ODT precedente.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Guarda anche

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
