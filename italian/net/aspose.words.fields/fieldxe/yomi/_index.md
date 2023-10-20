---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: Aspose.Words per .NET
description: FieldXE Yomi proprietà. Ottiene o imposta lo yomi primo carattere fonetico per lordinamento degli indici per la voce dellindice in C#.
type: docs
weight: 80
url: /it/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Ottiene o imposta lo yomi (primo carattere fonetico per l'ordinamento degli indici) per la voce dell'indice

```csharp
public string Yomi { get; set; }
```

## Esempi

Mostra come ordinare foneticamente le voci del campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE a destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text".
// in una voce invece di creare una voce per ciascun campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// La tabella INDEX ordina automaticamente le sue voci in base ai valori delle relative proprietà Text in ordine alfabetico.
// Imposta invece la tabella INDEX per ordinare le voci foneticamente utilizzando Hiragana.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Inserisci 4 campi XE, che verranno visualizzati come voci nel sommario del campo INDICE.
// La proprietà "Text" può contenere l'ortografia di una parola in Kanji, la cui pronuncia può essere ambigua,
// mentre la versione "Yomi" della parola si scriverà esattamente come viene pronunciata usando Hiragana.
// Se impostiamo il nostro campo INDEX per utilizzare Yomi, ordinerà queste voci
// in base al valore delle loro proprietà Yomi, anziché ai valori di testo.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Guarda anche

* class [FieldXE](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
