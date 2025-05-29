---
title: MailMergeRegionInfo.StartField
linktitle: StartField
articleTitle: StartField
second_title: Aspose.Words für .NET
description: Entdecken Sie die StartField-Eigenschaft von MailMergeRegionInfo – rufen Sie effizient das Startfeld für Ihre Seriendruckbereiche ab und optimieren Sie Ihre Dokumentautomatisierung.
type: docs
weight: 90
url: /de/net/aspose.words.mailmerging/mailmergeregioninfo/startfield/
---
## MailMergeRegionInfo.StartField property

Gibt ein Startfeld für die Region zurück.

```csharp
public FieldMergeField StartField { get; }
```

## Beispiele

Zeigt, wie Serienbriefbereiche überprüft werden.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Gibt eine vollständige Hierarchie von Zusammenführungsbereichen zurück, die im Dokument verfügbare MERGEFIELDs enthalten.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Top-Regionen im Dokument abrufen.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Verschachtelte Region in der ersten oberen Region abrufen.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Liste der Felder innerhalb der ersten oberen Region abrufen.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Siehe auch

* class [FieldMergeField](../../../aspose.words.fields/fieldmergefield/)
* class [MailMergeRegionInfo](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
