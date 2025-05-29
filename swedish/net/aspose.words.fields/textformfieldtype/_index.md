---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Fields.TextFormFieldType, som definierar olika typer av textformulärfält för förbättrad dokumentautomation och anpassning.
type: docs
weight: 3180
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
| Regular | `0` | Textformulärfältet kan innehålla valfri text. |
| Number | `1` | Textfältet i formuläret kan endast innehålla siffror. |
| Date | `2` | Textformulärfältet kan endast innehålla ett giltigt datumvärde. |
| CurrentDate | `3` | Värdet för textformulärfältet är det aktuella datumet då fältet uppdateras. |
| CurrentTime | `4` | Värdet för textformulärfältet är den aktuella tidpunkten då fältet uppdateras. |
| Calculated | `5` | Värdet för textformulärfältet beräknas från uttrycket som anges i [`TextInputDefault`](../formfield/textinputdefault/) egendom. |

## Exempel

Visar hur man skapar formulärfält.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Formulärfält är objekt i dokumentet som användaren kan interagera med genom att bli ombedd att ange värden.
// Vi kan skapa dem med hjälp av en dokumentbyggare, och nedan följer två sätt att göra det.
// 1 - Grundläggande textinmatning:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Kombinationsruta med prompttext och ett intervall av möjliga värden:
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
