---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con il metodo InsertHyperlink di DocumentBuilder, aggiungendo senza sforzo link cliccabili per una migliore navigazione e un maggiore coinvolgimento dell'utente.
type: docs
weight: 390
url: /it/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Inserisce un collegamento ipertestuale nel documento.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| displayText | String | Testo del collegamento da visualizzare nel documento. |
| urlOrBookmark | String | Destinazione del link. Può essere un URL o il nome di un segnalibro all'interno del documento. Questo metodo aggiunge sempre apostrofi all'inizio e alla fine dell'URL. |
| isBookmark | Boolean | `VERO` se il parametro precedente è il nome di un segnalibro all'interno del documento; `falso` il parametro precedente è un URL. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

## Osservazioni

Si noti che è necessario specificare esplicitamente la formattazione del carattere per il testo visualizzato nel collegamento ipertestuale utilizzando il[`Font`](../font/) proprietà.

Questo metodo chiama internamente[`InsertField`](../insertfield/)per inserire un campo COLLEGAMENTO IPERTESTUALE di MS Word nel documento.

## Esempi

Mostra come inserire un campo collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserisci un collegamento ipertestuale ed evidenzialo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Facendo clic con il tasto sinistro del mouse sul collegamento nel testo in Microsoft Word verremo indirizzati all'URL tramite una nuova finestra del browser Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
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

Mostra come utilizzare lo stack di formattazione di un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta la formattazione del carattere, quindi scrivi il testo che precede il collegamento ipertestuale.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Manteniamo la nostra attuale configurazione di formattazione sullo stack.
builder.PushFont();

// Modifica la formattazione corrente del builder applicando un nuovo stile.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Ripristina la formattazione del font salvata in precedenza e rimuove l'elemento dallo stack.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
