---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words für .NET
description: Passen Sie Ihre Revisionskommentare mit der Eigenschaft „RevisionOptions MeasurementUnit“ an. Legen Sie Maßeinheiten einfach fest, wobei Zentimeter die Standardeinstellung sind.
type: docs
weight: 80
url: /de/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Der Standardwert istCentimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

## Beispiele

Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
