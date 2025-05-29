---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.MailMerging.MailMergeRegionInfo per una gestione efficiente della stampa unione. Sblocca subito l'automazione perfetta dei documenti!
type: docs
weight: 4550
url: /it/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Contiene informazioni su un'area di stampa unione.

Per saperne di più, visita il[Unione di posta e creazione di report](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class MailMergeRegionInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Restituisce un campo finale per la regione. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Restituisce un tag "baffi" finale per la regione. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Restituisce un elenco di campi figlio. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Restituisce il livello di nidificazione per la regione. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Restituisce un elenco di tag figlio "baffi". |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Restituisce il nome della regione. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Restituisce informazioni sulla regione padre (null per la regione di livello superiore). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Restituisce un elenco di regioni figlio. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Restituisce un campo iniziale per la regione. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Restituisce un tag iniziale "baffi" per la regione. |

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

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)
