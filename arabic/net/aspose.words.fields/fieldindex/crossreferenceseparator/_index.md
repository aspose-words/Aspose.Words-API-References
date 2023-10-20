---
title: FieldIndex.CrossReferenceSeparator
linktitle: CrossReferenceSeparator
articleTitle: CrossReferenceSeparator
second_title: Aspose.Words لـ .NET
description: FieldIndex CrossReferenceSeparator ملكية. الحصول على أو تعيين تسلسل الأحرف المستخدم لفصل المراجع الترافقية والمدخلات الأخرى في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

الحصول على أو تعيين تسلسل الأحرف المستخدم لفصل المراجع الترافقية والمدخلات الأخرى.

```csharp
public string CrossReferenceSeparator { get; set; }
```

## أمثلة

يوضح كيفية تحديد المراجع الترافقية في حقل INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سيقوم إدخال INDEX بجمع كافة حقول XE ذات القيم المطابقة في خاصية "النص".
// في إدخال واحد بدلاً من عمل إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// يمكننا تكوين حقل XE للحصول على إدخال INDEX الخاص به لعرض سلسلة بدلاً من رقم الصفحة.
// أولاً، بالنسبة للإدخالات التي تستبدل رقم الصفحة بسلسلة،
// تحديد فاصل مخصص بين قيمة خاصية النص لحقل XE والسلسلة.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// أدخل حقل XE، مما يؤدي إلى إنشاء إدخال INDEX عادي يعرض رقم صفحة هذا الحقل،
// ولا يستدعي قيمة CrossReferenceSeparator.
// سيعرض إدخال حقل XE هذا "Apple، 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// أدخل حقل XE آخر في الصفحة 3 وقم بتعيين قيمة لخاصية PageNumberReplacement.
// ستظهر هذه القيمة بدلاً من رقم الصفحة التي يوجد بها هذا الحقل،
// وستظهر قيمة CrossReferenceSeparator لحقل INDEX أمامه.
// سيعرض الإدخال الخاص بحقل XE هذا "الموز، انظر: الفاكهة الاستوائية".
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

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
