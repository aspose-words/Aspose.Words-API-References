---
title: Class MailMergeRegionInfo
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.MailMerging.MailMergeRegionInfo فصل. يحتوي على معلومات حول منطقة دمج المراسلات .
type: docs
weight: 3640
url: /ar/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

يحتوي على معلومات حول منطقة دمج المراسلات .

```csharp
public class MailMergeRegionInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | إرجاع حقل نهاية للمنطقة . |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | إرجاع قائمة بالحقول الفرعية . |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | إرجاع مستوى التداخل للمنطقة. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | إرجاع اسم المنطقة . |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | إرجاع معلومات المنطقة الأصلية (خالية لمنطقة المستوى الأعلى) . |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | إرجاع قائمة بالمناطق الفرعية . |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | إرجاع حقل بداية للمنطقة . |

### أمثلة

يوضح كيفية التحقق من مناطق دمج البريد.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// إرجاع التسلسل الهرمي الكامل لمناطق الدمج التي تحتوي على MERGEFIELDs المتوفرة في المستند.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// احصل على أهم المناطق في المستند.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// احصل على منطقة متداخلة في أول منطقة أعلى.
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

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)


