---
title: MailMerge.GetRegionsByName
linktitle: GetRegionsByName
articleTitle: GetRegionsByName
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة MailMerge GetRegionsByName لاسترداد مجموعة من مناطق دمج البريد حسب الاسم بسهولة، مما يعزز أتمتة المستندات لديك.
type: docs
weight: 240
url: /ar/net/aspose.words.mailmerging/mailmerge/getregionsbyname/
---
## MailMerge.GetRegionsByName method

يعيد مجموعة من مناطق دمج البريد بالاسم المحدد.

```csharp
public IList<MailMergeRegionInfo> GetRegionsByName(string regionName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| regionName | String | اسم المنطقة (غير حساس لحالة الأحرف). |

### قيمة الإرجاع

قائمة المناطق.

## أمثلة

يوضح كيفية إنشاء مناطق دمج البريد وإدراجها وقراءتها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// علامتي "TableStart" و"TableEnd"، اللتين تدخلان داخل MERGEFIELDs،
// تشير إلى السلاسل التي تشير إلى بدايات ونهايات مناطق دمج البريد.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// استخدم هذه العلامات لبدء وإنهاء منطقة دمج البريد المسماة "MailMergeRegion1"،
// والتي سوف تحتوي على MERGEFIELDs لعمودين.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// يمكننا متابعة مناطق الدمج وأعمدتها من خلال النظر إلى هذه المجموعات.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// أدخل منطقة بنفس الاسم داخل المنطقة الموجودة، مما سيجعلها منطقة رئيسية.
// الآن سيكون حقل "Column2" داخل منطقة جديدة.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// إذا بحثنا عن اسم المناطق المكررة باستخدام طريقة "GetRegionsByName"،
// سوف يقوم بإرجاع جميع هذه المناطق في المجموعة.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// تأكد من أن المنطقة الثانية لديها الآن منطقة رئيسية.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### أنظر أيضا

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
