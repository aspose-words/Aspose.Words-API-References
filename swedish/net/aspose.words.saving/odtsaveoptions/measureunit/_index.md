---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words för .NET
description: Anpassa dokumentets MeasureUnit med OdtSaveOptions. Välj dina föredragna måttenheter för precision – standard är Centimeter.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Gör det möjligt att ange måttenheter som ska tillämpas på dokumentinnehåll. Standardvärdet ärCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Anmärkningar

Open Office använder centimeter när man anger längder, bredder och annan mätbar formatering och innehållsegenskaper i dokument medan MS Office använder tum.

## Exempel

Visar hur man använder olika måttenheter för att definiera stilparametrar för ett sparat ODT-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi exporterar dokumentet till .odt kan vi använda ett OdtSaveOptions-objekt för att ändra hur vi sparar dokumentet.
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Centimeters"
 // för att definiera innehåll såsom stilparametrar med hjälp av det metriska systemet, som Open Office använder.
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Inches"
// för att definiera innehåll såsom stilparametrar med hjälp av det imperiala systemet, vilket Microsoft Word använder.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Se även

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
