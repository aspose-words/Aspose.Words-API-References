---
title: Document.LastSection
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene lultima sezione del documento.
type: docs
weight: 220
url: /it/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Ottiene l'ultima sezione del documento.

```csharp
public Section LastSection { get; }
```

### Osservazioni

Restituisce`nullo` se non ci sono sezioni.

### Esempi

Mostra come creare una nuova sezione con un generatore di documenti.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione per impostazione predefinita,
// che contiene nodi figlio che possiamo modificare.
Assert.AreEqual(1, doc.Sections.Count);

// Usa un generatore di documenti per aggiungere testo alla prima sezione.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea una seconda sezione inserendo un'interruzione di sezione.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Ogni sezione ha le proprie impostazioni di configurazione della pagina.
// Possiamo dividere il testo nella seconda sezione in due colonne.
// Ciò non influirà sul testo nella prima sezione.
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
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


