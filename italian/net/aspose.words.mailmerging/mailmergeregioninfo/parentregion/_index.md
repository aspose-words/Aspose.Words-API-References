---
title: MailMergeRegionInfo.ParentRegion
second_title: Aspose.Words per .NET API Reference
description: MailMergeRegionInfo proprietà. Restituisce le informazioni sulla regione padre null per la regione di primo livello.
type: docs
weight: 50
url: /it/net/aspose.words.mailmerging/mailmergeregioninfo/parentregion/
---
## MailMergeRegionInfo.ParentRegion property

Restituisce le informazioni sulla regione padre (null per la regione di primo livello).

```csharp
public MailMergeRegionInfo ParentRegion { get; }
```

### Esempi

Mostra come creare, elencare e leggere le regioni di stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tag "TableStart" e "TableEnd", che vanno all'interno di MERGEFIELD,
// indica le stringhe che indicano l'inizio e la fine delle regioni di stampa unione.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Usa questi tag per avviare e terminare una regione di stampa unione denominata "MailMergeRegion1",
// che conterrà MERGEFIELD per due colonne.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Possiamo tenere traccia delle regioni di unione e delle relative colonne esaminando queste raccolte.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Inserisce una regione con lo stesso nome all'interno della regione esistente, che la renderà padre.
// Ora un campo "Colonna2" sarà all'interno di una nuova regione.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Se cerchiamo il nome delle regioni duplicate usando il metodo "GetRegionsByName",
// restituirà tutte queste regioni in una raccolta.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Verifica che la seconda regione abbia ora una regione padre.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Guarda anche

* class [MailMergeRegionInfo](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* assemblea [Aspose.Words](../../../)


