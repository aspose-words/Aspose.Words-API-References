---
title: FieldIndex.CrossReferenceSeparator
linktitle: CrossReferenceSeparator
articleTitle: CrossReferenceSeparator
second_title: Aspose.Words per .NET
description: FieldIndex CrossReferenceSeparator proprietà. Ottiene o imposta la sequenza di caratteri utilizzata per separare i riferimenti incrociati e altre voci in C#.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

Ottiene o imposta la sequenza di caratteri utilizzata per separare i riferimenti incrociati e altre voci.

```csharp
public string CrossReferenceSeparator { get; set; }
```

## Esempi

Mostra come definire i riferimenti incrociati in un campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE a destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text".
// in una voce invece di creare una voce per ciascun campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Possiamo configurare un campo XE per fare in modo che la sua voce INDEX visualizzi una stringa invece di un numero di pagina.
// Innanzitutto, per le voci che sostituiscono un numero di pagina con una stringa,
// specifica un separatore personalizzato tra il valore della proprietà Text del campo XE e la stringa.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Inserisci un campo XE, che crea una normale voce INDEX che visualizza il numero di pagina di questo campo,
// e non richiama il valore CrossReferenceSeparator.
// La voce per questo campo XE visualizzerà "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Inserisci un altro campo XE a pagina 3 e imposta un valore per la proprietà PageNumberReplacement.
// Questo valore verrà visualizzato al posto del numero della pagina in cui si trova questo campo,
// e il valore CrossReferenceSeparator del campo INDEX verrà visualizzato davanti ad esso.
// La voce per questo campo XE visualizzerà "Banana, vedi: Frutto tropicale".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
