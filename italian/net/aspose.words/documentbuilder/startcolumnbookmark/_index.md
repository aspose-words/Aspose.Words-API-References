---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words per .NET
description: DocumentBuilder StartColumnBookmark metodo. Contrassegna la posizione corrente nel documento come inizio di un segnalibro di colonna. La posizione deve essere in una cella della tabella in C#.
type: docs
weight: 620
url: /it/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Contrassegna la posizione corrente nel documento come inizio di un segnalibro di colonna. La posizione deve essere in una cella della tabella.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Nome del segnalibro. |

### Valore di ritorno

Il nodo iniziale del segnalibro appena creato.

## Osservazioni

Un segnalibro di colonna copre una o più colonne in un intervallo di righe. Per creare un segnalibro valido devi chiamarli entrambi`StartColumnBookmark` E[`EndColumnBookmark`](../endcolumnbookmark/) con lo stesso *bookmarkName*parametro.

I segnalibri formati in modo errato o i segnalibri con nomi duplicati verranno ignorati quando il documento viene salvato.

La posizione effettiva dell'inserito[`BookmarkStart`](../../bookmarkstart/) il nodo potrebbe differire dalla posizione corrente del document builder.

## Esempi

Mostra come creare un segnalibro di colonna.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Le celle 1,2,4,5 verranno aggiunte ai segnalibri.
builder.StartColumnBookmark("MyBookmark_1");
// I segnalibri formati in modo errato o i segnalibri con nomi duplicati verranno ignorati quando il documento viene salvato.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### Guarda anche

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
