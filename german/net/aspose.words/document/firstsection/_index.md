---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: Aspose.Words für .NET
description: Rufen Sie mühelos den ersten Abschnitt Ihres Dokuments ab. Verbessern Sie Ihren Workflow mit unserer Document FirstSection-Funktion für eine optimierte Organisation.
type: docs
weight: 140
url: /de/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Ruft den ersten Abschnitt im Dokument ab.

```csharp
public Section FirstSection { get; }
```

## Bemerkungen

Rückgaben`null`wenn keine Abschnitte vorhanden sind.

## Beispiele

Zeigt, wie Text in der Fußzeile eines Dokuments ersetzt wird.

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

Zeigt, wie mit einem Dokumentgenerator ein neuer Abschnitt erstellt wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält standardmäßig einen Abschnitt,
// die untergeordnete Knoten enthalten, die wir bearbeiten können.
Assert.AreEqual(1, doc.Sections.Count);

// Verwenden Sie einen Dokumentgenerator, um dem ersten Abschnitt Text hinzuzufügen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie einen zweiten Abschnitt, indem Sie einen Abschnittsumbruch einfügen.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Jeder Abschnitt hat seine eigenen Seiteneinrichtungseinstellungen.
// Wir können den Text im zweiten Abschnitt in zwei Spalten aufteilen.
// Dies hat keine Auswirkungen auf den Text im ersten Abschnitt.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

Zeigt, wie die untergeordneten Elemente eines zusammengesetzten Knotens durchlaufen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Ein Abschnitt ist ein zusammengesetzter Knoten und kann untergeordnete Knoten enthalten.
// aber nur, wenn diese untergeordneten Knoten vom Knotentyp „Body“ oder „HeaderFooter“ sind.
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

### Siehe auch

* class [Section](../../section/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
