---
title: FieldIndex.UseYomi
second_title: Aspose.Words لمراجع .NET API
description: FieldIndex ملكية. الحصول على أو تعيين ما إذا كان سيتم تمكين استخدام نص yomi لإدخالات الفهرس.
type: docs
weight: 170
url: /ar/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

الحصول على أو تعيين ما إذا كان سيتم تمكين استخدام نص yomi لإدخالات الفهرس.

```csharp
public bool UseYomi { get; set; }
```

### أمثلة

يوضح كيفية فرز إدخالات حقل INDEX صوتيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سيقوم إدخال INDEX بجمع كافة حقول XE ذات القيم المطابقة في خاصية "النص".
// في إدخال واحد بدلاً من عمل إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// يقوم جدول INDEX تلقائيًا بفرز إدخالاته حسب قيم خصائص النص الخاصة بها بالترتيب الأبجدي.
// قم بتعيين جدول INDEX لفرز الإدخالات صوتيًا باستخدام Hiragana بدلاً من ذلك.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// أدخل 4 حقول XE، والتي ستظهر كمدخلات في جدول محتويات حقل INDEX.
// قد تحتوي خاصية "النص" على تهجئة الكلمة باللغة الكانجي، والتي قد يكون نطقها غامضًا،
// في حين أن نسخة "Yomi" من الكلمة سوف توضح بالضبط كيفية نطقها باستخدام هيراغانا.
// إذا قمنا بتعيين حقل INDEX الخاص بنا لاستخدام Yomi، فسوف يقوم بفرز هذه الإدخالات
// بقيمة خصائص Yomi الخاصة بها، بدلاً من قيمها النصية.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### أنظر أيضا

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldindex/)
* المجسم [Aspose.Words](../../../)


