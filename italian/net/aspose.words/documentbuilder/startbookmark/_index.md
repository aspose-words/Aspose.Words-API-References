---
title: DocumentBuilder.StartBookmark
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Contrassegna la posizione corrente nel documento come inizio segnalibro.
type: docs
weight: 620
url: /it/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Contrassegna la posizione corrente nel documento come inizio segnalibro.

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Nome del segnalibro. |

### Valore di ritorno

Il nodo iniziale del segnalibro appena creato.

### Osservazioni

I segnalibri in un documento possono sovrapporsi e estendersi su qualsiasi intervallo. Per creare un segnalibro valido devi chiamarli entrambi`StartBookmark` E[`EndBookmark`](../endbookmark/) con lo stesso*bookmarkName* parametro .

I segnalibri formati in modo errato o i segnalibri con nomi duplicati verranno ignorati quando il documento viene salvato.

### Esempi

Mostra come creare un segnalibro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un segnalibro valido deve avere il testo del corpo del documento racchiuso da
// Nodi BookmarkStart e BookmarkEnd creati con un nome di segnalibro corrispondente.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Mostra come inserire un collegamento ipertestuale che fa riferimento a un segnalibro locale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Inserisci un campo HYPERLINK che si collega al segnalibro. Possiamo passare gli scambi di campo
// al metodo "InsertHyperlink" come parte dell'argomento contenente il nome del segnalibro di riferimento.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Guarda anche

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


