---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi alla proprietà FootnoteSeparatorCollection Item per recuperare facilmente FootnoteSeparators personalizzati in base al tipo, migliorando la formattazione del documento.
type: docs
weight: 20
url: /it/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Recupera un[`FootnoteSeparator`](../../footnoteseparator/) del tipo specificato.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Osservazioni

Restituisce`null` se il separatore di note a piè di pagina/note di chiusura del tipo specificato non viene trovato.

## Esempi

Mostra come gestire il formato del separatore delle note a piè di pagina.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Allinea il separatore delle note a piè di pagina.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Guarda anche

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
