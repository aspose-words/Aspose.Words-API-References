---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words för .NET
description: Lägg enkelt till textfält i formuläret med DocumentBuilder-metoden InsertTextInput. Förbättra ditt dokuments interaktivitet och användarupplevelse idag!
type: docs
weight: 510
url: /sv/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Infogar ett textformulärfält på den aktuella positionen.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Namnet på formulärfältet. Kan vara en tom sträng. |
| type | TextFormFieldType | Anger typen av textformulärfält. |
| format | String | Formatsträng som används för att formatera värdet i formulärfältet. |
| fieldValue | String | Text som kommer att visas i fältet. |
| maxLength | Int32 | Maximal längd som användaren kan ange i formulärfältet. Ställ in på noll för obegränsad längd. |

### Returvärde

Formulärfältnoden som just infogades.

## Anmärkningar

Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

## Exempel

Visar hur man infogar ett textinmatningsfält i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett formulär som uppmanar användaren att ange text.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Visar hur man infogar ett textinmatningsfält i formuläret.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Infoga ett textinmatningsfält som gör att användaren kan klicka på det och skriva in text.
// Tilldela platsmarkörtext som användaren kan skriva över och skicka vidare
// en maximal textlängd på 0 för att inte tillämpa någon gräns för formulärfältets innehåll.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Formulärfältet kommer att visas i form av en "input" html-tagg, med typen "text".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
