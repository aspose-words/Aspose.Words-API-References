---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.MeasurementUnits-uppräkning för exakt enhetsval i dokumentbehandling. Förbättra ditt arbetsflöde med exakta mätalternativ!
type: docs
weight: 4840
url: /sv/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Anger måttenheten.

```csharp
public enum MeasurementUnits
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Inches | `0` | Tum. |
| Centimeters | `1` | Centimeter. |
| Millimeters | `2` | Millimeter. |
| Points | `3` | Poäng. |
| Picas | `4` | Pica (vanligtvis används i traditionella skrivmaskiners teckensnittsavstånd). |

## Exempel

Visar hur man får ett sparat dokument att överensstämma med ett äldre ODT-schema.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
