---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: Aspose.Words لـ .NET
description: قم بتحسين إدخالات الفهرس لديك باستخدام خاصية Yomi في FieldXE، مما يتيح الفرز الفعال باستخدام الحرف الصوتي الأول لتحسين تنظيم البيانات.
type: docs
weight: 80
url: /ar/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

يحصل على أو يعين yomi (الحرف الصوتي الأول لفرز الفهارس) لإدخال الفهرس

```csharp
public string Yomi { get; set; }
```

## أمثلة

يوضح كيفية فرز إدخالات حقل INDEX صوتيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سوف يقوم إدخال INDEX بجمع جميع حقول XE ذات القيم المطابقة في خاصية "النص"
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// يقوم جدول INDEX تلقائيًا بفرز إدخالاته حسب قيم خصائص النص الخاصة بها بالترتيب الأبجدي.
// قم بتعيين جدول INDEX لفرز الإدخالات صوتيًا باستخدام Hiragana بدلاً من ذلك.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// أدخل 4 حقول XE، والتي ستظهر كإدخالات في جدول محتويات حقل INDEX.
// قد تحتوي خاصية "النص" على تهجئة كلمة في كانجي، وقد يكون نطقها غامضًا،
// في حين أن نسخة "Yomi" من الكلمة ستكتب بالضبط كما يتم نطقها باستخدام الهيراجانا.
// إذا قمنا بتعيين حقل INDEX الخاص بنا لاستخدام Yomi، فسوف يقوم بفرز هذه الإدخالات
// حسب قيمة خصائص Yomi الخاصة بهم، بدلاً من قيم Text الخاصة بهم.
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

* class [FieldXE](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
