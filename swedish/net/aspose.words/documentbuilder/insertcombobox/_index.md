---
title: DocumentBuilder.InsertComboBox
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Infogar ett formulärfält i kombinationsrutan på den aktuella positionen.
type: docs
weight: 280
url: /sv/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Infogar ett formulärfält i kombinationsrutan på den aktuella positionen.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Namnet på formulärfältet. Kan vara en tom sträng. Värdet längre än 20 tecken kommer att trunkeras. |
| items | String[] | Föremålen i ComboBox. Maximalt är 25 artiklar. |
| selectedIndex | Int32 | Indexet för det valda objektet i ComboBox. |

### Returvärde

Formulärfältsnoden som precis infogades.

### Anmärkningar

Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

### Exempel

Visar hur man infogar ett formulärfält med kombinationsruta i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett formulär som uppmanar användaren att välja ett av objekten från menyn.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


