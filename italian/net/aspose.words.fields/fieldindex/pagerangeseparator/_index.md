---
title: FieldIndex.PageRangeSeparator
linktitle: PageRangeSeparator
articleTitle: PageRangeSeparator
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageRangeSeparator in FieldIndex. Personalizza facilmente la sequenza di caratteri per una formattazione fluida degli intervalli di pagina e migliora la chiarezza del tuo documento.
type: docs
weight: 130
url: /it/net/aspose.words.fields/fieldindex/pagerangeseparator/
---
## FieldIndex.PageRangeSeparator property

Ottiene o imposta la sequenza di caratteri utilizzata per separare l'inizio e la fine di un intervallo di pagine.

```csharp
public string PageRangeSeparator { get; set; }
```

## Esempi

Mostra come specificare le pagine estese di un segnalibro come intervallo di pagine per una voce di campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Testo"
// in una voce anziché creare una voce per ogni campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Per le voci INDEX che visualizzano intervalli di pagine, possiamo specificare una stringa di separazione
// che apparirà tra il numero della prima pagina e il numero dell'ultima.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Se un campo XE assegna un nome a un segnalibro utilizzando la proprietà PageRangeBookmarkName,
// la sua voce INDICE mostrerà l'intervallo di pagine che il segnalibro copre
// invece del numero della pagina che contiene il campo XE.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Inserisci un segnalibro che inizia a pagina 3 e finisce a pagina 5.
// La voce INDICE per il campo XE che fa riferimento a questo segnalibro visualizzerà questo intervallo di pagine.
// Nella nostra tabella, la voce INDICE visualizzerà "La mia voce, nelle pagine da 3 a 5".
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
