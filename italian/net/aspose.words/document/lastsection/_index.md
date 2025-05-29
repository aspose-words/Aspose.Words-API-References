---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà LastSection per accedere facilmente alla sezione finale del tuo documento, migliorando l'efficienza della navigazione e della gestione dei contenuti.
type: docs
weight: 250
url: /it/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Ottiene l'ultima sezione del documento.

```csharp
public Section LastSection { get; }
```

## Osservazioni

Restituisce`null`se non ci sono sezioni.

## Esempi

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

### Guarda anche

* class [Section](../../section/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
