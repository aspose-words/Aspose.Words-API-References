---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.MeasurementUnits für die präzise Einheitenauswahl bei der Dokumentenverarbeitung. Verbessern Sie Ihren Workflow mit präzisen Messoptionen!
type: docs
weight: 4840
url: /de/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Gibt die Maßeinheit an.

```csharp
public enum MeasurementUnits
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Inches | `0` | Zoll. |
| Centimeters | `1` | Zentimeter. |
| Millimeters | `2` | Millimeter. |
| Points | `3` | Punkte. |
| Picas | `4` | Picas (üblicherweise im Schriftabstand herkömmlicher Schreibmaschinen verwendet). |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
