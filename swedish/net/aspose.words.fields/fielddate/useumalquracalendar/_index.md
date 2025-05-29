---
title: FieldDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldDate UseUmAlQuraCalendar för att enkelt hantera datum med UmalQura-kalendern. Förbättra din datumhantering idag!
type: docs
weight: 50
url: /sv/net/aspose.words.fields/fielddate/useumalquracalendar/
---
## FieldDate.UseUmAlQuraCalendar property

Hämtar eller anger om Um-al-Qura-kalendern ska användas.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Exempel

Visar hur man använder DATUM-fält för att visa datum enligt olika typer av kalendrar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi vill att texten i dokumentet alltid ska visa rätt datum kan vi använda ett DATUM-fält.
// Nedan följer tre typer av kulturella kalendrar som ett DATE-fält kan använda för att visa ett datum.
// 1 - Islamisk månkalender:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Umm al-Qura-kalendern:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Indisk nationalkalender:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Infoga ett DATUM-fält och ange dess kalendertyp till den som senast användes av värdapplikationen.
// I Microsoft Word är typen den senast använda i dialogrutan Infoga -> Text -> Datum och tid.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Se även

* class [FieldDate](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
