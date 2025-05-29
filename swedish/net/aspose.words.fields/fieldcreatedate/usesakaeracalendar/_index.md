---
title: FieldCreateDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldCreateDate UseSakaEraCalendar för att enkelt hantera Saka Era-kalenderinställningar i dina applikationer för förbättrad datumhantering.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

Hämtar eller anger om Saka-erans kalender ska användas.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Exempel

Visar hur man använder fältet SKAPADATUM för att visa dokumentets skapandedatum/-tid.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Vi kan använda fältet CREATEDATE för att visa datum och tid för skapandet av dokumentet.
// Nedan visas tre olika kalendertyper enligt vilka fältet CREATEDATE kan visa datum/tid.
// 1 - Islamisk månkalender:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura-kalendern:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Indisk nationalkalender:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Se även

* class [FieldCreateDate](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
