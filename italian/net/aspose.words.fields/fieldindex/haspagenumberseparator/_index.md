---
title: FieldIndex.HasPageNumberSeparator
linktitle: HasPageNumberSeparator
articleTitle: HasPageNumberSeparator
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldIndex HasPageNumberSeparator, che rivela se un separatore del numero di pagina è personalizzato tramite codice di campo per una formattazione avanzata del documento.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldindex/haspagenumberseparator/
---
## FieldIndex.HasPageNumberSeparator property

Ottiene un valore che indica se un separatore del numero di pagina viene sovrascritto tramite il codice del campo.

```csharp
public bool HasPageNumberSeparator { get; }
```

## Esempi

Mostra come modificare il separatore del numero di pagina in un campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Testo"
// in una voce anziché creare una voce per ogni campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Se il nostro campo INDICE ha una voce per un gruppo di campi XE,
// questa voce visualizzerà il numero di ogni pagina che contiene un campo XE appartenente a questo gruppo.
// Possiamo impostare separatori personalizzati per personalizzare l'aspetto di questi numeri di pagina.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// Dopo aver inserito questi campi XE, il campo INDICE visualizzerà "Prima voce, nelle pagine 2, 3 e 4".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
