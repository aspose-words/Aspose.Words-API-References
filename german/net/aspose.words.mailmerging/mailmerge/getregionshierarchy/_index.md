---
title: MailMerge.GetRegionsHierarchy
linktitle: GetRegionsHierarchy
articleTitle: GetRegionsHierarchy
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMerge GetRegionsHierarchy-Methode, um mühelos eine vollständige Regionshierarchie mit zugänglichen Dokumentfeldern für optimierte Arbeitsabläufe abzurufen.
type: docs
weight: 250
url: /de/net/aspose.words.mailmerging/mailmerge/getregionshierarchy/
---
## MailMerge.GetRegionsHierarchy method

Gibt eine vollständige Hierarchie der im Dokument verfügbaren Regionen (mit Feldern) zurück.

```csharp
public MailMergeRegionInfo GetRegionsHierarchy()
```

### Rückgabewert

Hierarchie der Regionen.

## Bemerkungen

Die Hierarchie wird zurückgegeben in Form von[`MailMergeRegionInfo`](../../mailmergeregioninfo/) Klasse.

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

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
