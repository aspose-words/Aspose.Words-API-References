---
title: FieldXE.Text
second_title: Aspose.Words لمراجع .NET API
description: FieldXE ملكية. الحصول على نص الإدخال أو تعيينه.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

الحصول على نص الإدخال أو تعيينه.

```csharp
public string Text { get; set; }
```

### أمثلة

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

يوضح كيفية تعبئة حقل INDEX بالإدخالات باستخدام حقول XE، وكذلك تعديل مظهره.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها،
// سيقوم حقل INDEX بتجميعها في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// سيؤدي تعيين قيمة هذه الخاصية إلى "A" إلى تجميع كافة الإدخالات حسب الحرف الأول منها،
// ثم ضع هذا الحرف بأحرف كبيرة فوق كل مجموعة.
index.Heading = "A";

// قم بتعيين الجدول الذي تم إنشاؤه بواسطة حقل INDEX ليمتد على عمودين.
index.NumberOfColumns = "2";

// قم بتعيين أي إدخالات بأحرف البداية خارج نطاق الأحرف "ac" ليتم حذفها.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// سيظهر حقلا XE التاليان تحت العنوان "A"،
// مع تطبيق أنماط النص الخاصة بها أيضًا على أرقام صفحاتها.
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

// سيكون حقلي XE التاليين تحت عنوان "B" و"C" في جدول محتويات حقول INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// تقوم حقول INDEX بفرز جميع الإدخالات أبجديًا، لذلك سيظهر هذا الإدخال ضمن "A" مع الإدخالين الآخرين.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// لن يظهر هذا الإدخال لأنه يبدأ بالحرف "D"،
// الذي يقع خارج نطاق الأحرف "ac" الذي تحدده خاصية LetterRange في حقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### أنظر أيضا

* class [FieldXE](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldxe/)
* المجسم [Aspose.Words](../../../)


