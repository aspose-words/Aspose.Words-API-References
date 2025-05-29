---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Notes.FootnoteSeparatorCollection per accedere facilmente ai separatori delle note a piè di pagina nei tuoi documenti. Migliora la formattazione dei tuoi documenti oggi stesso!
type: docs
weight: 5000
url: /it/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Fornisce accesso tipizzato a[`FootnoteSeparator`](../footnoteseparator/) nodi di un documento.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Recupera un[`FootnoteSeparator`](../footnoteseparator/) del tipo specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Esempi

Mostra come gestire il formato del separatore delle note a piè di pagina.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Allinea il separatore delle note a piè di pagina.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Guarda anche

* class [FootnoteSeparator](../footnoteseparator/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
