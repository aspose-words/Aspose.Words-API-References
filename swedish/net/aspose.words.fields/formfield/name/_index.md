---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt hanterar egenskapen FormField Name för att anpassa och optimera dina formulär för bättre användarengagemang och datainsamling.
type: docs
weight: 130
url: /sv/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Hämtar eller anger formulärfältets namn.

```csharp
public string Name { get; set; }
```

## Anmärkningar

Microsoft Word tillåter strängar med högst 20 tecken.

## Exempel

Visar hur man infogar en kombinationsruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Formulärfältet kommer att visas i form av en "select" html-tagg.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Se även

* class [FormField](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
