---
title: MailMerge.GetFieldNamesForRegion
linktitle: GetFieldNamesForRegion
articleTitle: GetFieldNamesForRegion
second_title: Aspose.Words per .NET
description: Scopri il metodo GetFieldNamesForRegion di MailMerge per accedere facilmente a una raccolta di nomi di campi di stampa unione nella regione specificata. Semplifica il tuo flusso di lavoro!
type: docs
weight: 230
url: /it/net/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## GetFieldNamesForRegion(*string*) {#getfieldnamesforregion}

Restituisce una raccolta di nomi di campi di unione di posta disponibili nella regione.

```csharp
public string[] GetFieldNamesForRegion(string regionName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| regionName | String | Nome della regione (senza distinzione tra maiuscole e minuscole). |

## Osservazioni

Restituisce i nomi completi dei campi unione, incluso il prefisso facoltativo. Non elimina i nomi di campo duplicati.

Se il documento contiene più regioni con lo stesso nome, verrà elaborata sempre la prima regione.

A ogni chiamata viene creato un nuovo array di stringhe.

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

---

## GetFieldNamesForRegion(*string, int*) {#getfieldnamesforregion_1}

Restituisce una raccolta di nomi di campi di unione di posta disponibili nella regione.

```csharp
public string[] GetFieldNamesForRegion(string regionName, int regionIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| regionName | String | Nome della regione (senza distinzione tra maiuscole e minuscole). |
| regionIndex | Int32 | Indice regionale (a partire da zero). |

## Osservazioni

Restituisce i nomi completi dei campi unione, incluso il prefisso facoltativo. Non elimina i nomi di campo duplicati.

Se il documento contiene più regioni con lo stesso nome, viene elaborata la regione N-esima (a partire da zero).

A ogni chiamata viene creato un nuovo array di stringhe.

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
