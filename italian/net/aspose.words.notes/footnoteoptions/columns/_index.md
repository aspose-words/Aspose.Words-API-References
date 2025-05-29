---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words per .NET
description: Scopri la proprietà Colonne di FootnoteOptions per formattare facilmente le note a piè di pagina con layout di colonne personalizzabili per una migliore leggibilità e presentazione.
type: docs
weight: 10
url: /it/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Specifica il numero di colonne con cui è formattata l'area delle note a piè di pagina.

```csharp
public int Columns { get; set; }
```

## Osservazioni

Se questa proprietà ha il valore 0, l'area delle note a piè di pagina viene formattata con un numero di colonne basato sul numero di colonne della pagina visualizzata. Il valore predefinito è 0.

## Esempi

Mostra come suddividere la sezione delle note a piè di pagina in un dato numero di colonne.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Guarda anche

* class [FootnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
