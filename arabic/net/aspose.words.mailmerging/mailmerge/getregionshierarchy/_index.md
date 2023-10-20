---
title: MailMerge.GetRegionsHierarchy
linktitle: GetRegionsHierarchy
articleTitle: GetRegionsHierarchy
second_title: Aspose.Words لـ .NET
description: MailMerge GetRegionsHierarchy طريقة. يُرجع التسلسل الهرمي الكامل للمناطق مع الحقول المتوفرة في المستند في C#.
type: docs
weight: 250
url: /ar/net/aspose.words.mailmerging/mailmerge/getregionshierarchy/
---
## MailMerge.GetRegionsHierarchy method

يُرجع التسلسل الهرمي الكامل للمناطق (مع الحقول) المتوفرة في المستند.

```csharp
public MailMergeRegionInfo GetRegionsHierarchy()
```

### قيمة الإرجاع

التسلسل الهرمي للمناطق.

## ملاحظات

يتم إرجاع التسلسل الهرمي في شكل[`MailMergeRegionInfo`](../../mailmergeregioninfo/) فصل.

## أمثلة

يوضح كيفية التحقق من مناطق دمج البريد.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// إرجاع تسلسل هرمي كامل لمناطق الدمج التي تحتوي على MERGEFIELDs المتوفرة في المستند.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// احصل على المناطق العليا في المستند.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// احصل على المنطقة المتداخلة في المنطقة العليا الأولى.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);

// احصل على قائمة الحقول داخل المنطقة العلوية الأولى.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### أنظر أيضا

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
