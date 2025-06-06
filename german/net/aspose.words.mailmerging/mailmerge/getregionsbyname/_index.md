---
title: MailMerge.GetRegionsByName
linktitle: GetRegionsByName
articleTitle: GetRegionsByName
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMerge-Methode „GetRegionsByName“, um mühelos eine Sammlung von Serienbriefbereichen nach Namen abzurufen und so Ihre Dokumentautomatisierung zu verbessern.
type: docs
weight: 240
url: /de/net/aspose.words.mailmerging/mailmerge/getregionsbyname/
---
## MailMerge.GetRegionsByName method

Gibt eine Sammlung von Serienbriefbereichen mit dem angegebenen Namen zurück.

```csharp
public IList<MailMergeRegionInfo> GetRegionsByName(string regionName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| regionName | String | Name der Region (ohne Berücksichtigung der Groß-/Kleinschreibung). |

### Rückgabewert

Die Liste der Regionen.

## Beispiele

Zeigt, wie Serienbriefbereiche erstellt, aufgelistet und gelesen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// „TableStart“- und „TableEnd“-Tags, die in MERGEFIELDs eingefügt werden,
// bezeichnen die Zeichenfolgen, die den Anfang und das Ende von Serienbriefbereichen kennzeichnen.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Verwenden Sie diese Tags, um einen Serienbriefbereich mit dem Namen „MailMergeRegion1“ zu starten und zu beenden.
// das MERGEFIELDs für zwei Spalten enthält.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Wir können Zusammenführungsbereiche und ihre Spalten verfolgen, indem wir uns diese Sammlungen ansehen.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Fügen Sie eine Region mit demselben Namen in die vorhandene Region ein, wodurch diese zu einer übergeordneten Region wird.
// Jetzt befindet sich ein „Column2“-Feld in einer neuen Region.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Wenn wir den Namen doppelter Regionen mit der Methode „GetRegionsByName“ nachschlagen,
// es werden alle derartigen Regionen in einer Sammlung zurückgegeben.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Überprüfen Sie, ob die zweite Region jetzt eine übergeordnete Region hat.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Siehe auch

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
