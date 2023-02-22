---
title: OdtSaveOptions.MeasureUnit
second_title: Aspose.Words för .NET API Referens
description: OdtSaveOptions fast egendom. Tillåter att ange måttenheter som ska tillämpas på dokumentinnehåll. Standardvärdet ärCentimeters
type: docs
weight: 30
url: /sv/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Tillåter att ange måttenheter som ska tillämpas på dokumentinnehåll. Standardvärdet ärCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

### Anmärkningar

Open Office använder centimeter när de anger längder, bredder och andra mätbara formaterings- och innehållsegenskaper i dokument medan MS Office använder tum.

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../odtsaveoptions/)
* hopsättning [Aspose.Words](../../../)


