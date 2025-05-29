---
title: FieldDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words för .NET
description: Optimera din datumhantering med FieldDates UseLunarCalendar-egenskap. Växla enkelt mellan Hijri- och hebreiska månkalendrar för förbättrad funktionalitet.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fielddate/uselunarcalendar/
---
## FieldDate.UseLunarCalendar property

Hämtar eller anger om Hijri-månkalendern eller den hebreiska månkalendern ska användas.

```csharp
public bool UseLunarCalendar { get; set; }
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
