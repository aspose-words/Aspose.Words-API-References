---
title: MailMergeRegionInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اسم MailMergeRegionInfo، التي تسترجع بشكل فعال اسم منطقة محددة لأتمتة المستندات بشكل سلس.
type: docs
weight: 60
url: /ar/net/aspose.words.mailmerging/mailmergeregioninfo/name/
---
## MailMergeRegionInfo.Name property

يعيد اسم المنطقة.

```csharp
public string Name { get; }
```

## أمثلة

يوضح كيفية التحقق من مناطق دمج البريد.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

//إرجاع التسلسل الهرمي الكامل لمناطق الدمج التي تحتوي على MERGEFIELDs المتوفرة في المستند.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// احصل على أفضل المناطق في المستند.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// احصل على المنطقة المتداخلة في المنطقة العلوية الأولى.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// الحصول على قائمة الحقول داخل المنطقة العلوية الأولى.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### أنظر أيضا

* class [MailMergeRegionInfo](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
