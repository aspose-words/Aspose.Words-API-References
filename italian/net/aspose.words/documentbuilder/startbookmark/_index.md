---
title: DocumentBuilder.StartBookmark
linktitle: StartBookmark
articleTitle: StartBookmark
second_title: Aspose.Words per .NET
description: Utilizza il metodo StartBookmark di DocumentBuilder per contrassegnare e gestire senza sforzo le posizioni chiave nel tuo documento, migliorando l'organizzazione e la navigazione.
type: docs
weight: 650
url: /it/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Contrassegna la posizione corrente nel documento come inizio del segnalibro.

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Nome del segnalibro. |

### Valore di ritorno

Il nodo di avvio del segnalibro appena creato.

## Osservazioni

I segnalibri in un documento possono sovrapporsi e coprire qualsiasi intervallo. Per creare un segnalibro valido è necessario chiamare entrambi`StartBookmark` E[`EndBookmark`](../endbookmark/) con lo stesso*bookmarkName* Parametro .

I segnalibri mal formattati o con nomi duplicati verranno ignorati quando il documento verrà salvato.

## Esempi

Mostra come creare un segnalibro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un segnalibro valido deve avere il testo del corpo del documento racchiuso tra
// I nodi BookmarkStart e BookmarkEnd vengono creati con un nome di segnalibro corrispondente.
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

// Inserisci un campo HYPERLINK che si collega al segnalibro. Possiamo passare degli switch di campo
// al metodo "InsertHyperlink" come parte dell'argomento contenente il nome del segnalibro a cui si fa riferimento.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Guarda anche

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
