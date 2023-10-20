---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words per .NET
description: Document IncludeTextboxesFootnotesEndnotesInStat proprietà. Specifica se includere caselle di testo note a piè di pagina e note di chiusura nelle statistiche sul conteggio delle parole in C#.
type: docs
weight: 220
url: /it/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Specifica se includere caselle di testo, note a piè di pagina e note di chiusura nelle statistiche sul conteggio delle parole.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Esempi

Mostra come includere o escludere caselle di testo, note a piè di pagina e note di chiusura dalle statistiche sul conteggio delle parole.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Per impostazione predefinita l'opzione è impostata su "false".
doc.UpdateWordCount();
// Le parole contano senza caselle di testo, note a piè di pagina e note di chiusura.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Le parole contano con caselle di testo, note a piè di pagina e note di chiusura.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
