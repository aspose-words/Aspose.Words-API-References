---
title: BuiltInDocumentProperties.RevisionNumber
second_title: Aspose.Words för .NET API Referens
description: BuiltInDocumentProperties fast egendom. Hämtar eller ställer in dokumentets revisionsnummer.
type: docs
weight: 240
url: /sv/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

Hämtar eller ställer in dokumentets revisionsnummer.

```csharp
public int RevisionNumber { get; set; }
```

### Anmärkningar

Aspose.Words uppdaterar inte den här egenskapen.

### Exempel

Visar hur man arbetar med REVNUM-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Infoga ett REVNUM-fält som visar dokumentets aktuella versionsnummeregenskap.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Den här egenskapen räknar hur många gånger ett dokument har sparats i Microsoft Word,
// och är inte relaterat till spårade revisioner. Vi kan hitta det genom att högerklicka på dokumentet i Utforskaren
// via Egenskaper -> Detaljer. Vi kan uppdatera den här egenskapen manuellt.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

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

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../builtindocumentproperties/)
* hopsättning [Aspose.Words](../../../)


