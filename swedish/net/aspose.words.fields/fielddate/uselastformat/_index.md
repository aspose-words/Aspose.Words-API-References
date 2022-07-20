---
title: UseLastFormat
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in om ett format som senast användes av värdapplikationen ska användas när ett nytt DATUM-fält infogas.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Hämtar eller ställer in om ett format som senast användes av värdapplikationen ska användas när ett nytt DATUM-fält infogas.

```csharp
public bool UseLastFormat { get; set; }
```

### Exempel

Visar hur du använder DATUM-fält för att visa datum enligt olika typer av kalendrar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi vill att texten i dokumentet alltid ska visa korrekt datum kan vi använda ett DATUM-fält.
// Nedan finns tre typer av kulturkalendrar som ett DATUMfält kan använda för att visa ett datum.
// 1 - Islamisk månkalender:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Umm al-Qura kalender:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Indian National Calendar:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Infoga ett DATUM-fält och ställ in dess kalendertyp till den som senast användes av värdapplikationen.
// I Microsoft Word kommer typen att vara den senast använda i Infoga -> Text -> Dialogrutan Datum och tid.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Se även

* class [FieldDate](../../fielddate)
* namnutrymme [Aspose.Words.Fields](../../fielddate)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->