---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words per .NET
description: FieldIndex RunSubentriesOnSameLine proprietà. Ottiene o imposta se eseguire le voci secondarie nella stessa riga della voce principale in C#.
type: docs
weight: 140
url: /it/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Ottiene o imposta se eseguire le voci secondarie nella stessa riga della voce principale.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Esempi

Mostra come lavorare con le voci secondarie in un campo INDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE a destra.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text".
// in una voce invece di creare una voce per ciascun campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Campi XE che hanno una proprietà Text il cui valore diventa l'intestazione della voce INDEX.
// Se questo valore contiene due segmenti di stringa divisi da due punti (la voce INDEX tratterà :) delimitatore,
// il primo segmento è l'intestazione e il secondo segmento diventerà il sottotitolo.
// Il campo INDICE raggruppa prima le voci in ordine alfabetico, poi, se sono presenti più campi XE con lo stesso
// intestazioni, il campo INDICE li sottoraggrupperà ulteriormente in base ai valori di queste intestazioni.
// Possono esserci più livelli di sottoraggruppamento, a seconda di quante volte
// le proprietà Text dei campi XE vengono segmentate in questo modo.
// Per impostazione predefinita, un gruppo di voci di campo INDICE creerà una nuova riga per ogni sottointestazione all'interno di questo gruppo.
// Possiamo impostare il flag RunSubentriesOnSameLine su true per mantenere l'intestazione,
// e ogni sottotitolo del gruppo invece su una riga, il che renderà il campo INDEX più compatto.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Inserisci due campi XE, ciascuno su una nuova pagina e con la stessa intestazione denominata "Intestazione 1",
// che il campo INDEX utilizzerà per raggrupparli.
// Se RunSubentriesOnSameLine è false, la tabella INDEX creerà tre righe:
// una riga per l'intestazione di raggruppamento "Intestazione 1" e un'altra riga per ogni sottointestazione.
// Se RunSubentriesOnSameLine è true, la tabella INDEX creerà una tabella a riga singola
// voce che comprende l'intestazione e ogni sottointestazione.
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
