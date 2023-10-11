---
title: Document.LastSection
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Hämtar det sista avsnittet i dokumentet.
type: docs
weight: 240
url: /sv/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Hämtar det sista avsnittet i dokumentet.

```csharp
public Section LastSection { get; }
```

### Anmärkningar

Returnerar`null` om det inte finns några avsnitt.

### Exempel

Visar hur man skapar en ny sektion med en dokumentbyggare.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller en sektion som standard,
// som innehåller underordnade noder som vi kan redigera.
Assert.AreEqual(1, doc.Sections.Count);

// Använd en dokumentbyggare för att lägga till text i det första avsnittet.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Skapa en andra sektion genom att infoga en sektionsbrytning.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Varje avsnitt har sina egna sidinställningar.
// Vi kan dela upp texten i det andra avsnittet i två kolumner.
// Detta kommer inte att påverka texten i det första avsnittet.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### Se även

* class [Section](../../section/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


