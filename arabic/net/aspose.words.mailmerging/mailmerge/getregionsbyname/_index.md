---
title: MailMerge.GetRegionsByName
second_title: Aspose.Words لمراجع .NET API
description: MailMerge طريقة. إرجاع مجموعة من مناطق دمج البريد بالاسم المحدد.
type: docs
weight: 240
url: /ar/net/aspose.words.mailmerging/mailmerge/getregionsbyname/
---
## MailMerge.GetRegionsByName method

إرجاع مجموعة من مناطق دمج البريد بالاسم المحدد.

```csharp
public IList<MailMergeRegionInfo> GetRegionsByName(string regionName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| regionName | String | اسم المنطقة (غير حساس لحالة الأحرف). |

### قيمة الإرجاع

قائمة المناطق.

### أمثلة

يوضح كيفية إنشاء مناطق دمج المراسلات وسردها وقراءتها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "TableStart" و "TableEnd" ، اللتان تدخلان داخل MERGEFIELDs ،
// تشير إلى السلاسل التي تشير إلى بدايات ونهايات مناطق دمج البريد.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// استخدم هذه العلامات لبدء وإنهاء منطقة دمج المراسلات المسماة "MailMergeRegion1" ،
// التي ستحتوي على MERGEFIELDs لعمودين.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// يمكننا تتبع مناطق الدمج وأعمدتها من خلال النظر إلى هذه المجموعات.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// أدخل منطقة بنفس الاسم داخل المنطقة الحالية ، مما سيجعلها أمة.
// الآن سيكون حقل "Column2" داخل منطقة جديدة.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// إذا بحثنا عن اسم المناطق المكررة باستخدام طريقة "GetRegionsByName" ،
// سيعيد كل هذه المناطق في مجموعة.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// تحقق من أن المنطقة الثانية بها الآن منطقة أصلية.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### أنظر أيضا

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


