---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.MeasurementUnits per una selezione precisa delle unità di misura nell'elaborazione dei documenti. Migliora il tuo flusso di lavoro con opzioni di misurazione accurate!
type: docs
weight: 4840
url: /it/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Specifica l'unità di misura.

```csharp
public enum MeasurementUnits
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Inches | `0` | Pollici. |
| Centimeters | `1` | Centimetri. |
| Millimeters | `2` | Millimetri. |
| Points | `3` | Punti. |
| Picas | `4` | Pica (comunemente utilizzati nella spaziatura dei caratteri delle macchine da scrivere tradizionali). |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
