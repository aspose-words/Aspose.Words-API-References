---
title: Columns
second_title: Aspose.Words per .NET API Reference
description: Specifica il numero di colonne con cui è formattata larea delle note a piè di pagina.
type: docs
weight: 10
url: /it/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Specifica il numero di colonne con cui è formattata l'area delle note a piè di pagina.

```csharp
public int Columns { get; set; }
```

### Osservazioni

Se questa proprietà ha il valore 0, l'area delle note a piè di pagina viene formattata con un numero di colonne basato su il numero di colonne nella pagina visualizzata. Il valore predefinito è 0.

### Esempi

Mostra come dividere la sezione delle note a piè di pagina in un determinato numero di colonne.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Guarda anche

* class [FootnoteOptions](../../footnoteoptions)
* spazio dei nomi [Aspose.Words.Notes](../../footnoteoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
