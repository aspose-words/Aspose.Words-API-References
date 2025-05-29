---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldIndex EntryType لإدارة أنواع إدخالات الفهرس بكفاءة لتحسين الفهرسة وتحسين أداء البحث.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

يحصل على نوع إدخال الفهرس المستخدم لبناء الفهرس أو يعينه.

```csharp
public string EntryType { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر
// والصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE تحتوي على نفس القيمة في خاصية "النص" الخاصة بها،
// سوف يقوم حقل INDEX بتجميعهم في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// قم بتكوين حقل INDEX فقط لعرض حقول XE الموجودة ضمن الحدود
// لإشارة مرجعية تسمى "MainBookmark"، وخصائص "EntryType" الخاصة بها لها قيمة "A".
// بالنسبة لكلا الحقلين INDEX وXE، تستخدم خاصية "EntryType" الحرف الأول فقط من قيمة السلسلة الخاصة بها.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// في صفحة جديدة، ابدأ الإشارة المرجعية باسم يتطابق مع القيمة
// من خاصية "BookmarkName" في حقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// سوف يلتقط حقل INDEX هذا الإدخال لأنه موجود داخل الإشارة المرجعية،
// ونوع الإدخال الخاص به يتطابق أيضًا مع نوع إدخال حقل INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// أدخل حقل XE الذي لن يظهر في INDEX لأن أنواع الإدخالات لا تتطابق.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// قم بإنهاء الإشارة المرجعية وإدراج حقل XE بعد ذلك.
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
