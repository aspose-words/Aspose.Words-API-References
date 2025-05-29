---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldXE PageNumberReplacement per personalizzare facilmente il testo del numero di pagina, migliorando la formattazione del documento e la leggibilità.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Ottiene o imposta il testo utilizzato al posto di un numero di pagina.

```csharp
public string PageNumberReplacement { get; set; }
```

## Esempi

Mostra come definire i riferimenti incrociati in un campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Testo"
// in una voce anziché creare una voce per ogni campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Possiamo configurare un campo XE in modo che la sua voce INDICE visualizzi una stringa anziché un numero di pagina.
// Innanzitutto, per le voci che sostituiscono un numero di pagina con una stringa,
// specifica un separatore personalizzato tra il valore della proprietà Text del campo XE e la stringa.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Inserire un campo XE, che crea una voce INDICE regolare che visualizza il numero di pagina di questo campo,
// e non richiama il valore CrossReferenceSeparator.
// La voce per questo campo XE visualizzerà "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Inserire un altro campo XE a pagina 3 e impostare un valore per la proprietà PageNumberReplacement.
// Questo valore verrà visualizzato al posto del numero della pagina in cui si trova questo campo,
// e il valore CrossReferenceSeparator del campo INDEX apparirà davanti ad esso.
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

* class [FieldXE](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
