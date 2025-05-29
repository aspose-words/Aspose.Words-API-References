---
title: FieldXE.PageRangeBookmarkName
linktitle: PageRangeBookmarkName
articleTitle: PageRangeBookmarkName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldXE PageRangeBookmarkName—إدارة أسماء الإشارات المرجعية بكفاءة لتتبع نطاق الصفحات بدقة في مستنداتك.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldxe/pagerangebookmarkname/
---
## FieldXE.PageRangeBookmarkName property

يحصل على اسم الإشارة المرجعية التي تحدد نطاق الصفحات التي يتم إدراجها كرقم صفحة الإدخال أو يعينه.

```csharp
public string PageRangeBookmarkName { get; set; }
```

## أمثلة

يوضح كيفية تحديد الصفحات الممتدة للإشارة المرجعية كنطاق صفحة لإدخال حقل INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سوف يقوم إدخال INDEX بجمع جميع حقول XE ذات القيم المطابقة في خاصية "النص"
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// بالنسبة لإدخالات INDEX التي تعرض نطاقات الصفحات، يمكننا تحديد سلسلة فاصلة
//الذي سيظهر بين رقم الصفحة الأولى ورقم الصفحة الأخيرة.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// إذا قام حقل XE بتسمية إشارة مرجعية باستخدام خاصية PageRangeBookmarkName،
// سيعرض إدخال الفهرس نطاق الصفحات التي يغطيها الإشارة المرجعية
//بدلاً من رقم الصفحة التي تحتوي على حقل XE.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

//أدرج إشارة مرجعية تبدأ في الصفحة 3 وتنتهي في الصفحة 5.
// سيعرض إدخال INDEX لحقل XE الذي يشير إلى هذه الإشارة المرجعية نطاق الصفحة هذا.
// في جدولنا، سيعرض إدخال INDEX "إدخالي، في الصفحة (الصفحات) من 3 إلى 5".
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### أنظر أيضا

* class [FieldXE](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
