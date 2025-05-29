---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldSeq BookmarkName för att enkelt hantera dokumentnavigering. Ange eller hämta bokmärkesnamn för smidig objektreferens.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Hämtar eller anger ett bokmärkesnamn som refererar till ett objekt någon annanstans i dokumentet snarare än på den aktuella platsen.

```csharp
public string BookmarkName { get; set; }
```

## Exempel

Visar hur man kombinerar innehållsförtecknings- och sekvensfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett innehållsförteckningsfält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
// Varje post innehåller stycket som innehåller SEQ-fältet,
// och numret på sidan där fältet visas.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurera detta innehållsförteckningsfält så att det har en SequenceIdentifier-egenskap med värdet "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Konfigurera detta innehållsförteckningsfält för att endast hämta SEQ-fält som ligger inom gränserna för ett bokmärke
// med namnet "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata antal för varje unik namngiven sekvens
// identifierad av SEQ-fältets egenskap "SequenceIdentifier".
// Infoga ett SEQ-fält som har en sekvensidentifierare som matchar innehållsförteckningen
// egenskapen TableOfFiguresLabel. Det här fältet skapar inte en post i innehållsförteckningen eftersom det ligger utanför
// bokmärkets gränser angivna av "Bokmärkesnamn".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Sekvensen i detta SEQ-fält matchar egenskapen "TableOfFiguresLabel" i innehållsförteckningen och ligger inom bokmärkets gränser.
// Stycket som innehåller det här fältet kommer att visas i innehållsförteckningen som en post.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Sekvensen i detta SEQ-fält matchar inte egenskapen "TableOfFiguresLabel" i innehållsförteckningen.
// och ligger inom bokmärkets gränser. Dess stycke kommer inte att visas i innehållsförteckningen som en post.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Sekvensen i detta SEQ-fält matchar egenskapen "TableOfFiguresLabel" i innehållsförteckningen och ligger inom bokmärkets gränser.
// Detta fält refererar också till ett annat bokmärke. Innehållet i det bokmärket kommer att visas i innehållsförteckningen för detta sekvensfält.
// Själva SEQ-fältet visar inte innehållet i det bokmärket.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Skapa ett bokmärke med innehåll som visas i innehållsförteckningen på grund av att ovanstående SEQ-fält refererar till det.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Se även

* class [FieldSeq](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
