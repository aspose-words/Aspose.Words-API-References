---
title: FieldSaveDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words för .NET
description: Hantera dina datum enkelt med FieldSaveDate-egenskapen. Växla enkelt mellan UmalQura-kalendern för förbättrad schemaläggning och planering.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldsavedate/useumalquracalendar/
---
## FieldSaveDate.UseUmAlQuraCalendar property

Hämtar eller anger om Um-al-Qura-kalendern ska användas.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Exempel

Visar hur man använder fältet SPARADATUM för att visa datum/tid för dokumentets senaste sparningsåtgärd som utfördes med Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Vi kan använda fältet SAVEDATE för att visa datum och tid för den senaste sparningen i dokumentet.
// Sparoperationen som dessa fält refererar till är den manuella sparoperationen i ett program som Microsoft Word,
// inte dokumentets Spara-metod.
// Nedan visas tre olika kalendertyper enligt vilka fältet SPARADATUM kan visa datum/tid.
// 1 - Islamisk månkalender:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura-kalendern:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Indisk nationalkalender:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE-fälten hämtar sina datum-/tidsvärden från den inbyggda egenskapen LastSavedTime.
// Dokumentets Save-metod kommer inte att uppdatera detta värde, men vi kan fortfarande uppdatera det manuellt.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Se även

* class [FieldSaveDate](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
