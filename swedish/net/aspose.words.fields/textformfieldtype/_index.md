---
title: Enum TextFormFieldType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.TextFormFieldType uppräkning. Anger typen av ett textformulärfält.
type: docs
weight: 2590
url: /sv/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Anger typen av ett textformulärfält.

```csharp
public enum TextFormFieldType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Regular | `0` | Textformulärfältet kan innehålla vilken text som helst. |
| Number | `1` | Textformulärfältet kan endast innehålla siffror. |
| Date | `2` | Textformulärfältet kan endast innehålla ett giltigt datumvärde. |
| CurrentDate | `3` | Textformulärfältets värde är det aktuella datumet då fältet uppdateras. |
| CurrentTime | `4` | Textformulärfältets värde är den aktuella tidpunkten då fältet uppdateras. |
| Calculated | `5` | Textformulärfältets värde beräknas från uttrycket som anges i [`TextInputDefault`](../formfield/textinputdefault/) egenskap. |

### Exempel

Visar hur man skapar formulärfält.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Formulärfält är objekt i dokumentet som användaren kan interagera med genom att uppmanas att ange värden.
// Vi kan skapa dem med hjälp av en dokumentbyggare, och nedan finns två sätt att göra det.
// 1 - Grundläggande textinmatning:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Kombinationsruta med prompttext och en rad möjliga värden:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


