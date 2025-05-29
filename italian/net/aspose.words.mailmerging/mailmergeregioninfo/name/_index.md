---
title: MailMergeRegionInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la proprietà Name di MailMergeRegionInfo, che recupera in modo efficiente il nome di una regione specificata per un'automazione ottimale dei documenti.
type: docs
weight: 60
url: /it/net/aspose.words.mailmerging/mailmergeregioninfo/name/
---
## MailMergeRegionInfo.Name property

Restituisce il nome della regione.

```csharp
public string Name { get; }
```

## Esempi

Mostra come verificare le aree di unione dati.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Restituisce una gerarchia completa delle regioni di unione che contengono i MERGEFIELD disponibili nel documento.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Ottieni le regioni principali del documento.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Ottieni la regione nidificata nella prima regione superiore.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Ottieni l'elenco dei campi all'interno della prima regione superiore.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Guarda anche

* class [MailMergeRegionInfo](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
