---
title: Enum OdtSaveMeasureUnit
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.OdtSaveMeasureUnit uppräkning. Angivna måttenheter som ska tillämpas på mätbart dokumentinnehåll som form bredder och annat under sparandet.
type: docs
weight: 5320
url: /sv/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Angivna måttenheter som ska tillämpas på mätbart dokumentinnehåll som form, bredder och annat under sparandet.

```csharp
public enum OdtSaveMeasureUnit
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Centimeters | `0` | Anger att dokumentinnehållet sparas med centimeter. |
| Inches | `1` | Anger att dokumentinnehållet sparas med tum. |

### Exempel

Visar hur man använder olika måttenheter för att definiera stilparametrar för ett sparat ODT-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi exporterar dokumentet till .odt kan vi använda ett OdtSaveOptions-objekt för att ändra hur vi sparar dokumentet.
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Centimeters"
 // för att definiera innehåll som stilparametrar med hjälp av det metriska systemet, som Open Office använder.
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Inches"
// för att definiera innehåll som stilparametrar med hjälp av det imperialistiska systemet, som Microsoft Word använder.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


