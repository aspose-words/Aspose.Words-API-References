---
title: MailMerge.RegionStartTag
linktitle: RegionStartTag
articleTitle: RegionStartTag
second_title: Aspose.Words per .NET
description: Scopri la proprietà MailMerge RegionStartTag per definire e personalizzare facilmente le aree di stampa unione, migliorando il processo di automazione dei documenti.
type: docs
weight: 100
url: /it/net/aspose.words.mailmerging/mailmerge/regionstarttag/
---
## MailMerge.RegionStartTag property

Ottiene o imposta un tag di inizio regione di unione di posta.

```csharp
public string RegionStartTag { get; set; }
```

## Esempi

Mostra come creare, elencare e leggere le aree di stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tag "TableStart" e "TableEnd", che vanno all'interno dei MERGEFIELD,
// indica le stringhe che indicano l'inizio e la fine delle aree di stampa unione.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Utilizzare questi tag per iniziare e terminare un'area di stampa unione denominata "MailMergeRegion1",
// che conterrà i MERGEFIELD per due colonne.
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

// Inserisce una regione con lo stesso nome all'interno della regione esistente, che diventerà una regione padre.
// Ora un campo "Column2" sarà all'interno di una nuova regione.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Se cerchiamo il nome delle regioni duplicate utilizzando il metodo "GetRegionsByName",
// restituirà tutte queste regioni in una raccolta.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Verificare che la seconda regione abbia ora una regione padre.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
