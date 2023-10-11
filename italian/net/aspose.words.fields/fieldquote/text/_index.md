---
title: FieldQuote.Text
second_title: Aspose.Words per .NET API Reference
description: FieldQuote proprietà. Ottiene o imposta il testo da recuperare.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Ottiene o imposta il testo da recuperare.

```csharp
public string Text { get; set; }
```

### Esempi

Mostra di utilizzare il campo QUOTE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un campo QUOTE, che visualizzerà il valore della sua proprietà Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserisci un campo QUOTE e nidifica un campo DATA al suo interno.
// I campi DATA aggiornano il loro valore alla data corrente ogni volta che apriamo il documento utilizzando Microsoft Word.
// Nidificare il campo DATA all'interno del campo QUOTE in questo modo ne congelerà il valore
// alla data in cui abbiamo creato il documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Aggiorna tutti i campi per visualizzare i risultati corretti.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Guarda anche

* class [FieldQuote](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldquote/)
* assemblea [Aspose.Words](../../../)


