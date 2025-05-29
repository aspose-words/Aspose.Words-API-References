---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldIndex RunSubentriesOnSameLine per gestire facilmente le sottovoci in linea con le voci principali, per un'organizzazione dei dati semplificata.
type: docs
weight: 140
url: /it/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Ottiene o imposta se eseguire le sottovoci nella stessa riga della voce principale.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Esempi

Mostra come lavorare con le sottovoci in un campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Testo"
// in una voce anziché creare una voce per ogni campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Campi XE che hanno una proprietà Text il cui valore diventa l'intestazione della voce INDEX.
// Se questo valore contiene due segmenti di stringa divisi da due punti (la voce INDEX tratterà il delimitatore :),
// il primo segmento è il titolo, il secondo diventerà il sottotitolo.
// Il campo INDICE raggruppa prima le voci in ordine alfabetico, quindi, se ci sono più campi XE con lo stesso
// intestazioni, il campo INDICE le suddividerà ulteriormente in sottogruppi in base ai valori di queste intestazioni.
// Possono esserci più livelli di sottoraggruppamento, a seconda di quante volte
// le proprietà Testo dei campi XE vengono segmentate in questo modo.
// Per impostazione predefinita, un gruppo di voci di campo INDICE creerà una nuova riga per ogni sottotitolo all'interno di questo gruppo.
// Possiamo impostare il flag RunSubentriesOnSameLine su true per mantenere l'intestazione,
// e ogni sottotitolo del gruppo su una riga, il che renderà il campo INDICE più compatto.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Inserire due campi XE, ciascuno su una nuova pagina e con la stessa intestazione denominata "Intestazione 1",
// che il campo INDICE utilizzerà per raggrupparli.
// Se RunSubentriesOnSameLine è falso, la tabella INDEX creerà tre righe:
// una riga per il titolo di raggruppamento "Titolo 1" e un'altra riga per ogni sottotitolo.
// Se RunSubentriesOnSameLine è vero, la tabella INDEX creerà una riga
// voce che comprende il titolo e tutti i sottotitoli.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
