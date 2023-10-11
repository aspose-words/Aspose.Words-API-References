---
title: MailMerge.GetRegionsByName
second_title: Aspose.Words per .NET API Reference
description: MailMerge metodo. Restituisce una raccolta di regioni di stampa unione con il nome specificato.
type: docs
weight: 240
url: /it/net/aspose.words.mailmerging/mailmerge/getregionsbyname/
---
## MailMerge.GetRegionsByName method

Restituisce una raccolta di regioni di stampa unione con il nome specificato.

```csharp
public IList<MailMergeRegionInfo> GetRegionsByName(string regionName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| regionName | String | Nome della regione (senza distinzione tra maiuscole e minuscole). |

### Valore di ritorno

L'elenco delle regioni.

### Esempi

Mostra come creare, elencare e leggere le aree di stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I tag "TableStart" e "TableEnd", che vanno all'interno dei MERGEFIELD,
// denota le stringhe che indicano l'inizio e la fine delle regioni di stampa unione.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Utilizza questi tag per avviare e terminare una regione di stampa unione denominata "MailMergeRegion1",
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

// Inserisci una regione con lo stesso nome all'interno della regione esistente, che la renderà genitore.
// Ora un campo "Column2" sarà all'interno di una nuova regione.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Se cerchiamo il nome delle regioni duplicate utilizzando il metodo "GetRegionsByName",
// restituirà tutte queste regioni in una raccolta.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Controlla che la seconda regione ora abbia una regione principale.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Guarda anche

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


