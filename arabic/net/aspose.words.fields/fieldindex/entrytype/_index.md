---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words لـ .NET
description: FieldIndex EntryType ملكية. الحصول على أو تعيين نوع إدخال الفهرس المستخدم لإنشاء الفهرس في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

الحصول على أو تعيين نوع إدخال الفهرس المستخدم لإنشاء الفهرس.

```csharp
public string EntryType { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر
// والصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها،
// سيقوم حقل INDEX بتجميعها في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// قم بتكوين حقل INDEX فقط لعرض حقول XE الموجودة ضمن الحدود
// للإشارة المرجعية المسماة "MainBookmark"، والتي تحتوي خصائص "EntryType" الخاصة بها على قيمة "A".
// بالنسبة لكل من الحقلين INDEX وXE، تستخدم خاصية "EntryType" فقط الحرف الأول من قيمة السلسلة الخاصة بها.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// في صفحة جديدة، ابدأ الإشارة المرجعية باسم يطابق القيمة
// الخاصية "BookmarkName" الخاصة بحقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// سيلتقط حقل INDEX هذا الإدخال لأنه موجود داخل الإشارة المرجعية،
// ونوع الإدخال الخاص به يتطابق أيضًا مع نوع إدخال حقل INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// أدخل حقل XE الذي لن يظهر في الفهرس لأن أنواع الإدخال غير متطابقة.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// قم بإنهاء الإشارة المرجعية وأدخل حقل XE بعد ذلك.
// إنه من نفس نوع حقل INDEX، لكنه لن يظهر
// لأنه خارج حدود الإشارة المرجعية.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

### أنظر أيضا

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
