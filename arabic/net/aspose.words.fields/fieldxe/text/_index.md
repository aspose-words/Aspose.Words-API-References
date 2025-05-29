---
title: FieldXE.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: أدر خصائص نص FieldXE بسهولة. احصل على نص الإدخال أو عيّنه بسهولة لإدارة بياناتك بسلاسة وتحسين تجربة المستخدم.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

يحصل على نص الإدخال أو يعينه.

```csharp
public string Text { get; set; }
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

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وتعديل مظهره أيضًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE تحتوي على نفس القيمة في خاصية "النص" الخاصة بها،
// سوف يقوم حقل INDEX بتجميعهم في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// سيؤدي تعيين قيمة هذه الخاصية إلى "A" إلى تجميع جميع الإدخالات حسب الحرف الأول منها،
// ثم ضع هذا الحرف بأحرف كبيرة فوق كل مجموعة.
index.Heading = "A";

// قم بتعيين الجدول الذي تم إنشاؤه بواسطة حقل INDEX ليمتد على عمودين.
index.NumberOfColumns = "2";

// قم بتعيين أي إدخالات تحتوي على أحرف بداية خارج نطاق الأحرف "ac" ليتم حذفها.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// سيظهر حقلي XE التاليين تحت عنوان "A"،
// مع تطبيق أنماط النصوص الخاصة بهم أيضًا على أرقام صفحاتهم.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

//سيكون كلا الحقلين XE التاليين تحت عنواني "B" و"C" في جدول محتويات حقول INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// تقوم حقول INDEX بفرز جميع الإدخالات أبجديًا، بحيث يظهر هذا الإدخال تحت "A" مع الإدخالين الآخرين.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// لن يظهر هذا الإدخال لأنه يبدأ بالحرف "D"،
// وهو خارج نطاق الأحرف "ac" الذي تحدده خاصية LetterRange في حقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### أنظر أيضا

* class [FieldXE](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
