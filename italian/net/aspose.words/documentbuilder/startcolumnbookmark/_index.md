---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words per .NET
description: Utilizza il metodo StartColumnBookmark di DocumentBuilder per contrassegnare facilmente le posizioni delle celle della tabella come segnalibri di colonna, migliorando così la navigazione e l'organizzazione del documento.
type: docs
weight: 660
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

Il nodo di avvio del segnalibro appena creato.

## Osservazioni

Un segnalibro di colonna copre una o più colonne in un intervallo di righe. Per creare un segnalibro valido, è necessario chiamare entrambi`StartColumnBookmark` E[`EndColumnBookmark`](../endcolumnbookmark/) con lo stesso *bookmarkName* parametro.

I segnalibri mal formattati o con nomi duplicati verranno ignorati quando il documento verrà salvato.

La posizione effettiva dell'inserito[`BookmarkStart`](../../bookmarkstart/) il nodo potrebbe differire dalla posizione corrente del builder document .

## Esempi

Mostra come creare un segnalibro di colonna.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Le celle 1, 2, 4, 5 verranno aggiunte ai segnalibri.
builder.StartColumnBookmark("MyBookmark_1");
// I segnalibri mal formattati o con nomi duplicati verranno ignorati quando il documento verrà salvato.
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
