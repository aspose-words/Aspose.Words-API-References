---
title: FieldIndex.LetterRange
linktitle: LetterRange
articleTitle: LetterRange
second_title: Aspose.Words لـ .NET
description: FieldIndex LetterRange ملكية. الحصول على أو تعيين نطاق من الحروف التي تحدد الفهرس في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.fields/fieldindex/letterrange/
---
## FieldIndex.LetterRange property

الحصول على أو تعيين نطاق من الحروف التي تحدد الفهرس.

```csharp
public string LetterRange { get; set; }
```

## أمثلة

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

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
