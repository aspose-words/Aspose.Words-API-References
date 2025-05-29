---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldXE PageNumberReplacement لتخصيص نص رقم الصفحة بسهولة لتحسين تنسيق المستند وتحسين إمكانية القراءة.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

يحصل على النص المستخدم بدلاً من رقم الصفحة أو يعينه.

```csharp
public string PageNumberReplacement { get; set; }
```

## أمثلة

يوضح كيفية تعريف المراجع المتقاطعة في حقل INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سوف يقوم إدخال INDEX بجمع جميع حقول XE ذات القيم المطابقة في خاصية "النص"
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// يمكننا تكوين حقل XE للحصول على إدخال INDEX الخاص به لعرض سلسلة بدلاً من رقم الصفحة.
//أولاً، بالنسبة للإدخالات التي تستبدل رقم الصفحة بسلسلة،
// حدد فاصلًا مخصصًا بين قيمة خاصية النص في حقل XE والسلسلة.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// إدراج حقل XE، والذي ينشئ إدخال INDEX عادي يعرض رقم صفحة هذا الحقل،
// ولا يستدعي قيمة CrossReferenceSeparator.
// سيعرض إدخال حقل XE هذا "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// قم بإدراج حقل XE آخر في الصفحة 3 وقم بتعيين قيمة لخاصية PageNumberReplacement.
// ستظهر هذه القيمة بدلاً من رقم الصفحة التي يوجد بها هذا الحقل،
// وسوف تظهر قيمة CrossReferenceSeparator الخاصة بحقل INDEX أمامه.
// سيعرض إدخال حقل XE هذا "الموز، انظر: الفاكهة الاستوائية".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### أنظر أيضا

* class [FieldXE](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
