---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldIndex RunSubentriesOnSameLine لإدارة الإدخالات الفرعية بسهولة بما يتماشى مع الإدخالات الرئيسية لتنظيم البيانات بشكل مبسط.
type: docs
weight: 140
url: /ar/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

يحصل على أو يحدد ما إذا كان سيتم تشغيل الإدخالات الفرعية في نفس السطر مثل الإدخال الرئيسي.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## أمثلة

يوضح كيفية العمل مع الإدخالات الفرعية في حقل INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سوف يقوم إدخال INDEX بجمع جميع حقول XE ذات القيم المطابقة في خاصية "النص"
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// حقول XE التي تحتوي على خاصية نصية تصبح قيمتها عنوان إدخال INDEX.
// إذا كانت هذه القيمة تحتوي على قطعتين من السلسلة مقسمتين بعلامة نقطتين (سيتعامل إدخال INDEX مع الفاصل :)،
// الجزء الأول هو العنوان، والجزء الثاني سيصبح العنوان الفرعي.
// يقوم حقل INDEX أولاً بتجميع الإدخالات أبجديًا، ثم إذا كان هناك حقول XE متعددة بنفس
// العناوين، سيقوم حقل INDEX بتقسيمها بشكل إضافي حسب قيم هذه العناوين.
// يمكن أن يكون هناك طبقات تجميع فرعية متعددة، اعتمادًا على عدد المرات
// يتم تقسيم خصائص النص الخاصة بحقول XE على هذا النحو.
// بشكل افتراضي، ستقوم مجموعة إدخال حقل INDEX بإنشاء سطر جديد لكل عنوان فرعي ضمن هذه المجموعة.
// يمكننا ضبط علم RunSubentriesOnSameLine على true للاحتفاظ بالعنوان،
// وكل عنوان فرعي للمجموعة على سطر واحد بدلاً من ذلك، مما سيجعل حقل INDEX أكثر إحكاما.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// أدخل حقلين XE، كل منهما في صفحة جديدة، وبنفس العنوان المسمى "العنوان 1"،
// والتي سيستخدمها حقل INDEX لتجميعها.
// إذا كانت RunSubentriesOnSameLine خاطئة، فسوف يقوم جدول INDEX بإنشاء ثلاثة أسطر:
// سطر واحد لعنوان التجميع "العنوان 1"، وسطر آخر لكل عنوان فرعي.
// إذا كانت قيمة RunSubentriesOnSameLine صحيحة، فسوف يقوم جدول INDEX بإنشاء سطر واحد
// إدخال يشتمل على العنوان وكل عنوان فرعي.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### أنظر أيضا

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
