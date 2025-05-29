---
title: FieldXE.IsItalic
linktitle: IsItalic
articleTitle: IsItalic
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IsItalic di FieldXE migliora lo stile del tuo documento applicando facilmente la formattazione corsiva ai numeri di pagina, per un aspetto più curato.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldxe/isitalic/
---
## FieldXE.IsItalic property

Ottiene o imposta se applicare la formattazione corsiva al numero di pagina della voce.

```csharp
public bool IsItalic { get; set; }
```

## Esempi

Mostra come popolare un campo INDICE con voci utilizzando campi XE e come modificarne l'aspetto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDICE li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Impostando il valore di questa proprietà su "A" tutte le voci verranno raggruppate in base alla loro prima lettera,
// e posiziona quella lettera in maiuscolo sopra ogni gruppo.
index.Heading = "A";

// Imposta la tabella creata dal campo INDEX in modo che si estenda su 2 colonne.
index.NumberOfColumns = "2";

// Imposta l'omissione di tutte le voci con lettere iniziali al di fuori dell'intervallo di caratteri "ac".
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Questi due campi XE successivi verranno visualizzati sotto l'intestazione "A",
// con i rispettivi stili di testo applicati anche ai numeri di pagina.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// I due campi XE successivi saranno sotto le intestazioni "B" e "C" nella tabella dei contenuti dei campi INDICE.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// I campi INDEX ordinano tutte le voci in ordine alfabetico, quindi questa voce verrà visualizzata sotto "A" insieme alle altre due.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Questa voce non verrà visualizzata perché inizia con la lettera "D",
// che è al di fuori dell'intervallo di caratteri "ac" definito dalla proprietà LetterRange del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Guarda anche

* class [FieldXE](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
