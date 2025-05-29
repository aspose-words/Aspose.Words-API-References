---
title: FieldListNum.HasListName
linktitle: HasListName
articleTitle: HasListName
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FieldListNum HasListName indikerar om ett abstrakt numreringsdefinitionsnamn ingår i fältkoden för förbättrad dokumentformatering.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

Returnerar ett värde som anger om namnet på en abstrakt numreringsdefinition tillhandahålls av fältets kod.

```csharp
public bool HasListName { get; }
```

## Exempel

Visar hur man numrerar stycken med LISTNUM-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM-fält visar ett tal som ökar vid varje LISTNUM-fält.
// Dessa fält har också en mängd olika alternativ som gör att vi kan använda dem för att emulera numrerade listor.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listor börjar räknas på 1 som standard, men vi kan ställa in detta tal till ett annat värde, till exempel 0.
// Det här fältet visar "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// LISTNUM-fält har separata antal för varje listnivå.
// Infoga ett LISTNUM-fält i samma stycke som ett annat LISTNUM-fält
// ökar listnivån istället för antalet.
// Nästa fält fortsätter den räkning vi startade ovan och visar värdet "1" på listnivå 1.
builder.InsertField(FieldType.FieldListNum, true);

// Det här fältet startar en räkning på listnivå 2. Det visar värdet "1".
builder.InsertField(FieldType.FieldListNum, true);

// Det här fältet startar en räkning på listnivå 3. Det visar värdet "1".
// Olika listnivåer har olika formatering,
// så dessa fält kombinerat kommer att visa värdet "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Nästa LISTNUM-fält som vi infogar fortsätter räkningen på listnivå
// att det föregående LISTNUM-fältet var aktiverat.
// Vi kan använda egenskapen "ListLevel" för att hoppa till en annan listnivå.
// Om detta LISTNUM-fält förblev på listnivå 3 skulle det visa "ii)",
// men eftersom vi har flyttat den till listnivå 2 fortsätter den räkningen på den nivån och visar "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Vi kan ställa in egenskapen ListName för att få fältet att emulera en annan AUTONUM-fälttyp.
// "NumberDefault" emulerar AUTONUMM, "OutlineDefault" emulerar AUTONUMOUT,
// och "LegalDefault" emulerar AUTONUMLGL-fält.
// Listnamnet "OutlineDefault" med startnumret 1 kommer att resultera i att "I." visas.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName överförs inte från föregående fält, så vi måste ställa in det för varje nytt fält.
// Det här fältet fortsätter räkningen med det andra listnamnet och visar "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Se även

* class [FieldListNum](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
