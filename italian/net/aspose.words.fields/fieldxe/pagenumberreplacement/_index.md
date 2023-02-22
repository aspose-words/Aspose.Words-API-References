---
title: FieldXE.PageNumberReplacement
second_title: Aspose.Words per .NET API Reference
description: FieldXE proprietà. Ottiene o imposta il testo utilizzato al posto del numero di pagina.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Ottiene o imposta il testo utilizzato al posto del numero di pagina.

```csharp
public string PageNumberReplacement { get; set; }
```

### Esempi

Mostra come definire i riferimenti incrociati in un campo INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE a destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text".
// in una voce invece di inserire una voce per ogni campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Possiamo configurare un campo XE per ottenere la sua voce INDEX per visualizzare una stringa anziché un numero di pagina.
// Innanzitutto, per le voci che sostituiscono un numero di pagina con una stringa,
// specifica un separatore personalizzato tra il valore della proprietà Text del campo XE e la stringa.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Inserisci un campo XE, che crea una normale voce INDEX che mostra il numero di pagina di questo campo,
// e non richiama il valore CrossReferenceSeparator.
// La voce per questo campo XE visualizzerà "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Inserisce un altro campo XE a pagina 3 e imposta un valore per la proprietà PageNumberReplacement.
// Questo valore verrà visualizzato al posto del numero della pagina in cui si trova questo campo,
// e il valore CrossReferenceSeparator del campo INDEX apparirà davanti ad esso.
// La voce per questo campo XE visualizzerà "Banana, vedi: Frutto tropicale".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Guarda anche

* class [FieldXE](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldxe/)
* assemblea [Aspose.Words](../../../)


