---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FieldDate UseLastFormat förbättrar ditt arbetsflöde genom att behålla det senast använda datumformatet för sömlös integration i dina applikationer.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Hämtar eller anger om ett format som senast användes av värdapplikationen ska användas när ett nytt DATUM-fält infogas.

```csharp
public bool UseLastFormat { get; set; }
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
