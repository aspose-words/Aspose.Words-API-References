---
title: FieldIndex.HasSequenceName
linktitle: HasSequenceName
articleTitle: HasSequenceName
second_title: Aspose.Words för .NET
description: Upptäck om en sekvens behövs för effektiv fältresultatsgenerering med egenskapen FieldIndex HasSequenceName. Optimera din datahantering idag!
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldindex/hassequencename/
---
## FieldIndex.HasSequenceName property

Hämtar ett värde som anger om en sekvens ska användas medan fältets resultat skapas.

```csharp
public bool HasSequenceName { get; }
```

## Exempel

Visar hur man delar upp ett dokument i delar genom att kombinera INDEX- och SEQ-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för Text på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// Om XE-fälten har samma värde i sin "Text"-egenskap,
// INDEX-fältet grupperar dem i en post.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// I egenskapen SequenceName, namnge en SEQ-fältsekvens. Varje post i detta INDEX-fält kommer nu också att visas
// numret som sekvensräkningen är på vid XE-fältplatsen som skapade denna post.
index.SequenceName = "MySequence";

// Ställ in text som omger sekvens- och sidnummer för att förklara deras betydelse för användaren.
// En post som skapas med den här konfigurationen kommer att visa något i stil med "MySequence at 1 on page 1" vid sidnumret.
// PageNumberSeparator och SequenceSeparator får inte vara längre än 15 tecken.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata antal för varje unik namngiven sekvens
// identifierad av SEQ-fältets egenskap "SequenceIdentifier".
// Infoga ett SEQ-fält som flyttar sekvensen "MySequence" till 1.
// Detta fält skiljer sig inte från vanlig dokumenttext. Det kommer inte att visas i innehållsförteckningen för ett INDEX-fält.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Infoga ett XE-fält som skapar en post i INDEX-fältet.
// Eftersom "MySequence" är på 1 och detta XE-fält finns på sidan 2, tillsammans med de anpassade separatorerna vi definierade ovan,
// INDEX-posten i det här fältet visar "Katt" till vänster och "MinSekvens vid 1 på sidan 2" till höger.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Infoga en sidbrytning och använd SEQ-fält för att flytta "MySequence" till 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Infoga ett XE-fält med samma Text-egenskap som det ovan.
// INDEX-posten grupperar XE-fält med matchande värden i egenskapen "Text"
// till en post istället för att skapa en post för varje XE-fält.
// Eftersom vi är på sidan 2 med "MySequence" vid 3, kommer ",3 på sidan 3" att läggas till i samma INDEX-post som ovan.
// Sidnummerdelen av INDEX-posten visar nu "MySequence vid 1 på sidan 2, 3 på sidan 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Infoga ett XE-fält med ett nytt och unikt Text-egenskapsvärde.
// Detta lägger till en ny post, med MySequence vid 3 på sidan 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
