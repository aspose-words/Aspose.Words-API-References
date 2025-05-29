---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: Aspose.Words per .NET
description: Recupera la prima sezione del tuo documento senza sforzo. Migliora il tuo flusso di lavoro con la nostra proprietà Document FirstSection per un'organizzazione semplificata.
type: docs
weight: 140
url: /it/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Ottiene la prima sezione del documento.

```csharp
public Section FirstSection { get; }
```

## Osservazioni

Restituisce`null`se non ci sono sezioni.

## Esempi

Mostra come sostituire il testo nel piè di pagina di un documento.

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

Mostra come creare una nuova sezione con un generatore di documenti.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione per impostazione predefinita,
// che contiene nodi figlio che possiamo modificare.
Assert.AreEqual(1, doc.Sections.Count);

// Utilizzare un generatore di documenti per aggiungere testo alla prima sezione.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea una seconda sezione inserendo un'interruzione di sezione.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Ogni sezione ha le proprie impostazioni di impostazione della pagina.
// Possiamo dividere il testo nella seconda sezione in due colonne.
// Ciò non influirà sul testo della prima sezione.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

Mostra come scorrere gli elementi figlio di un nodo composito.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Una sezione è un nodo composito e può contenere nodi figlio,
// ma solo se tali nodi figlio sono di tipo "Body" o "HeaderFooter".
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

### Guarda anche

* class [Section](../../section/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
