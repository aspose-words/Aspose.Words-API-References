---
title: DocumentBuilder.EndColumnBookmark
linktitle: EndColumnBookmark
articleTitle: EndColumnBookmark
second_title: Aspose.Words per .NET
description: Utilizza il metodo EndColumnBookmark di DocumentBuilder per contrassegnare facilmente la fine di una colonna nel tuo documento. Migliora la gestione delle tabelle con precisione!
type: docs
weight: 220
url: /it/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

Contrassegna la posizione corrente nel documento come fine segnalibro di colonna. La posizione deve essere in una cella della tabella.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Nome del segnalibro. |

### Valore di ritorno

Il nodo finale del segnalibro appena creato.

## Osservazioni

Un segnalibro di colonna copre una o più colonne in un intervallo di righe. Per creare un segnalibro valido, è necessario chiamare entrambi[`StartColumnBookmark`](../startcolumnbookmark/) E`EndColumnBookmark` con lo stesso *bookmarkName* parametro.

I segnalibri mal formattati o con nomi duplicati verranno ignorati quando il documento verrà salvato.

La posizione effettiva dell'inserito[`BookmarkEnd`](../../bookmarkend/) il nodo potrebbe differire dalla posizione corrente del builder document .

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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
