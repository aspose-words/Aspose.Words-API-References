---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: Aspose.Words för .NET
description: Hämta den första delen av ditt dokument utan problem. Förbättra ditt arbetsflöde med vår egenskap DokumentförstaSektion för effektiv organisation.
type: docs
weight: 140
url: /sv/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Hämtar det första avsnittet i dokumentet.

```csharp
public Section FirstSection { get; }
```

## Anmärkningar

Returer`null`om det inte finns några sektioner.

## Exempel

Visar hur man ersätter text i ett dokuments sidfot.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

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

Visar hur man itererar igenom barnen till en sammansatt nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// En sektion är en sammansatt nod och kan innehålla undernoder,
// men bara om dessa undernoder är av nodtypen "Body" eller "HeaderFooter".
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### Se även

* class [Section](../../section/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
