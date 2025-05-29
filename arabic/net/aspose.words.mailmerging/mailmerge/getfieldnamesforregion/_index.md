---
title: MailMerge.GetFieldNamesForRegion
linktitle: GetFieldNamesForRegion
articleTitle: GetFieldNamesForRegion
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة MailMerge GetFieldNamesForRegion للوصول بسهولة إلى مجموعة من أسماء حقول دمج البريد في منطقتك المحددة. بسّط سير عملك!
type: docs
weight: 230
url: /ar/net/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## GetFieldNamesForRegion(*string*) {#getfieldnamesforregion}

يقوم بإرجاع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة.

```csharp
public string[] GetFieldNamesForRegion(string regionName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| regionName | String | اسم المنطقة (غير حساس لحالة الأحرف). |

## ملاحظات

يُرجع أسماء حقول الدمج كاملةً، بما في ذلك البادئة الاختيارية. لا يُلغي أسماء الحقول المكررة.

إذا كانت الوثيقة تحتوي على مناطق متعددة بنفس الاسم، فسيتم معالجة المنطقة الأولى.

يتم إنشاء مجموعة سلسلة جديدة في كل مكالمة.

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

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## GetFieldNamesForRegion(*string, int*) {#getfieldnamesforregion_1}

يقوم بإرجاع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة.

```csharp
public string[] GetFieldNamesForRegion(string regionName, int regionIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| regionName | String | اسم المنطقة (غير حساس لحالة الأحرف). |
| regionIndex | Int32 | مؤشر المنطقة (يبدأ من الصفر). |

## ملاحظات

يُرجع أسماء حقول الدمج كاملةً، بما في ذلك البادئة الاختيارية. لا يُلغي أسماء الحقول المكررة.

إذا كانت الوثيقة تحتوي على مناطق متعددة بنفس الاسم، فسيتم معالجة المنطقة N (التي تبدأ بالصفر).

يتم إنشاء مجموعة سلسلة جديدة في كل مكالمة.

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

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
