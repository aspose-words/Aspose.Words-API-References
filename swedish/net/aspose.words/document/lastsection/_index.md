---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LastSection för att enkelt komma åt den sista delen av ditt dokument, vilket förbättrar navigering och effektivitet i innehållshantering.
type: docs
weight: 250
url: /sv/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Hämtar det sista avsnittet i dokumentet.

```csharp
public Section LastSection { get; }
```

## Anmärkningar

Returer`null`om det inte finns några sektioner.

## Exempel

Visar hur man skapar ett nytt avsnitt med en dokumentbyggare.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller som standard en sektion,
// som innehåller underordnade noder som vi kan redigera.
Assert.AreEqual(1, doc.Sections.Count);

// Använd en dokumentbyggare för att lägga till text i det första avsnittet.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Skapa ett andra avsnitt genom att infoga en avsnittsbrytning.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Varje sektion har sina egna inställningar för sidinställningar.
// Vi kan dela upp texten i det andra avsnittet i två kolumner.
// Detta påverkar inte texten i det första avsnittet.
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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
