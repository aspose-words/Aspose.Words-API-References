---
title: FieldSaveDate.UseSakaEraCalendar
second_title: Aspose.Words för .NET API Referens
description: FieldSaveDate fast egendom. Hämtar eller ställer in om Saka Erakalendern ska användas.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldsavedate/usesakaeracalendar/
---
## FieldSaveDate.UseSakaEraCalendar property

Hämtar eller ställer in om Saka Era-kalendern ska användas.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

### Exempel

Visar hur du använder fältet SAVEDATE för att visa datum/tid för dokumentets senaste lagringsoperation utförd med Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Vi kan använda fältet SAVEDATE för att visa datum och tid för den senaste lagringsoperationen i dokumentet.
// Sparningsoperationen som dessa fält refererar till är den manuella lagringen i ett program som Microsoft Word,
// inte dokumentets spara-metod.
// Nedan finns tre olika kalendertyper enligt vilka fältet SAVEDATE kan visa datum/tid.
// 1 - Islamisk månkalender:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura kalender:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Indisk nationella kalender:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE-fälten hämtar sina datum/tidsvärden från den inbyggda egenskapen LastSavedTime.
// Dokumentets spara-metod kommer inte att uppdatera detta värde, men vi kan fortfarande uppdatera det manuellt.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Se även

* class [FieldSaveDate](../)
* namnutrymme [Aspose.Words.Fields](../../fieldsavedate/)
* hopsättning [Aspose.Words](../../../)


