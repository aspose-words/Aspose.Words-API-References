---
title: DocumentBuilder.InsertHyperlink
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un collegamento ipertestuale nel documento.
type: docs
weight: 340
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
| urlOrBookmark | String | Destinazione del collegamento. Può essere un URL o il nome di un segnalibro all'interno del documento. Questo metodo aggiunge sempre apostrofi all'inizio e alla fine dell'URL. |
| isBookmark | Boolean | True se il parametro precedente è il nome di un segnalibro all'interno del documento; false è il parametro precedente è un URL. |

### Valore di ritorno

UN[`Field`](../../../aspose.words.fields/field/) oggetto che rappresenta il campo inserito.

### Osservazioni

Si noti che è necessario specificare la formattazione del carattere per il testo visualizzato del collegamento ipertestuale in modo esplicito utilizzando l'estensione[`Font`](../font/) proprietà.

Questo metodo chiama internamente[`InsertField`](../insertfield/) per inserire un campo MS Word HYPERLINK nel documento.

### Esempi

Mostra come inserire un collegamento ipertestuale che fa riferimento a un segnalibro locale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Inserisce un campo HYPERLINK che si collega al segnalibro. Possiamo passare gli interruttori di campo
// al metodo "InsertHyperlink" come parte dell'argomento contenente il nome del segnalibro di riferimento.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Mostra come inserire un campo di collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserisci un collegamento ipertestuale ed enfatizzalo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic sinistro sul collegamento nel testo in Microsoft Word ci porterà all'URL tramite una nuova finestra del browser web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Mostra come utilizzare lo stack di formattazione di un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta la formattazione del carattere, quindi scrivi il testo che precede il collegamento ipertestuale.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Conserva la nostra attuale configurazione di formattazione nello stack.
builder.PushFont();

// Modifica la formattazione corrente del builder applicando un nuovo stile.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Ripristina la formattazione del carattere che abbiamo salvato in precedenza e rimuovi l'elemento dallo stack.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


