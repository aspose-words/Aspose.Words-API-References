---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.MailMerging.MailMergeRegionInfo لإدارة دمج البريد بكفاءة. تمتع بأتمتة مستندات سلسة اليوم!
type: docs
weight: 4550
url: /ar/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

يحتوي على معلومات حول منطقة دمج البريد.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class MailMergeRegionInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | يعيد حقل نهاية للمنطقة. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | يعيد علامة نهاية "الشارب" للمنطقة. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | يعيد قائمة من الحقول الفرعية. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | يعيد مستوى التعشيش للمنطقة. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | يعيد قائمة من علامات "الشارب" الفرعية. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | يعيد اسم المنطقة. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | إرجاع معلومات المنطقة الأصلية (null للمنطقة ذات المستوى الأعلى). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | يعيد قائمة بالمناطق الفرعية. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | يعيد حقل البداية للمنطقة. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | يعيد علامة "mustache" البداية للمنطقة. |

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

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
