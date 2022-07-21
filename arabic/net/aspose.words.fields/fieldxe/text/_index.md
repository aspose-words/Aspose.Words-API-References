---
title: Text
second_title: Aspose.Words لمراجع .NET API
description: الحصول على نص الإدخال أو تعيينه.
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

يوضح كيفية إنشاء حقل INDEX ، ثم استخدام حقول XE لملئه بالإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة الخاصية Text لحقل XE على الجانب الأيسر
// والصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها ،
// سيجمعها الحقل INDEX في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// تكوين الحقل INDEX فقط لعرض حقول XE الموجودة داخل الحدود
// من إشارة مرجعية مسماة "MainBookmark" ، وخصائصها "EntryType" لها قيمة "A".
// بالنسبة لكل من الحقول INDEX و XE ، تستخدم الخاصية "EntryType" فقط الحرف الأول من قيمة السلسلة الخاصة بها.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// في صفحة جديدة ، ابدأ الإشارة المرجعية باسم يطابق القيمة
// من خاصية "BookmarkName" للحقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// سوف يلتقط حقل INDEX هذا الإدخال لأنه داخل الإشارة المرجعية ،
// ونوع الإدخال الخاص به يتطابق أيضًا مع نوع إدخال الحقل INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// أدخل حقل XE لن يظهر في الفهرس لأن أنواع الإدخال غير متطابقة.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// قم بإنهاء الإشارة المرجعية وأدخل حقل XE بعد ذلك.
// إنه من نفس نوع الحقل INDEX ، لكنه لن يظهر
// لأنه خارج حدود الإشارة المرجعية.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

يوضح كيفية تعبئة حقل INDEX بإدخالات باستخدام حقول XE ، وكذلك تعديل مظهره.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية نص حقل XE على الجانب الأيسر ،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها ،
// سيجمعها الحقل INDEX في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// سيؤدي تعيين قيمة هذه الخاصية على "A" إلى تجميع جميع الإدخالات حسب الحرف الأول ،
// ووضع هذا الحرف بأحرف كبيرة فوق كل مجموعة.
index.Heading = "A";

// قم بتعيين الجدول الذي تم إنشاؤه بواسطة الحقل INDEX ليمتد على عمودين.
index.NumberOfColumns = "2";

// قم بتعيين أي إدخالات بأحرف بداية خارج نطاق أحرف "ac" ليتم حذفها.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// سيظهر حقلا XE التاليان تحت العنوان "A" ،
// مع أنماط النص الخاصة بهم تنطبق أيضًا على أرقام صفحاتهم.
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

// سيكون كلا حقلي XE التاليين تحت عنوان "B" و "C" في جدول محتويات حقول INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX الحقول تفرز جميع المدخلات أبجديًا ، لذلك سيظهر هذا الإدخال تحت "A" مع الاثنين الآخرين.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// لن يظهر هذا الإدخال لأنه يبدأ بالحرف "D" ،
// الذي يقع خارج نطاق الأحرف "ac" الذي تحدده خاصية LetterRange للحقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### أنظر أيضا

* class [FieldXE](../../fieldxe)
* مساحة الاسم [Aspose.Words.Fields](../../fieldxe)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
