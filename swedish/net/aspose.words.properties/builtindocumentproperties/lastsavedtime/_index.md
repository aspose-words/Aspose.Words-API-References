---
title: BuiltInDocumentProperties.LastSavedTime
linktitle: LastSavedTime
articleTitle: LastSavedTime
second_title: Aspose.Words för .NET
description: BuiltInDocumentProperties LastSavedTime fast egendom. Hämtar eller ställer in tiden för den senaste lagringen i UTC i C#.
type: docs
weight: 170
url: /sv/net/aspose.words.properties/builtindocumentproperties/lastsavedtime/
---
## BuiltInDocumentProperties.LastSavedTime property

Hämtar eller ställer in tiden för den senaste lagringen i UTC.

```csharp
public DateTime LastSavedTime { get; set; }
```

## Anmärkningar

För dokument som kommer från RTF-format returnerar den här egenskapen den lokala tiden för senaste lagring.

Aspose.Words uppdaterar inte den här egenskapen.

## Exempel

Visar hur man arbetar med dokumentegenskaper i kategorin "Ursprung".

```csharp
// Öppna ett dokument som vi har skapat och redigerat med Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Följande inbyggda egenskaper innehåller information om skapandet och redigeringen av detta dokument.
// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta
// dessa egenskaper via "Egenskaper" -> "Detaljer" -> "Ursprung" kategori.
// Fält som PRINTDATE och EDITTIME kan visa dessa värden i dokumentets brödtext.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Vi kan också ändra värden på inbyggda fastigheter.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word uppdaterar följande egenskaper automatiskt när vi sparar dokumentet.
// För att använda dessa egenskaper med Aspose.Words måste vi ställa in värden för dem manuellt.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

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

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
