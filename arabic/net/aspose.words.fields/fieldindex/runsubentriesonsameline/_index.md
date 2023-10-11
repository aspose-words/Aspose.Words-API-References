---
title: FieldIndex.RunSubentriesOnSameLine
second_title: Aspose.Words لمراجع .NET API
description: FieldIndex ملكية. يحصل على أو يحدد ما إذا كان سيتم تشغيل الإدخالات الفرعية في نفس سطر الإدخال الرئيسي.
type: docs
weight: 140
url: /ar/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

يحصل على أو يحدد ما إذا كان سيتم تشغيل الإدخالات الفرعية في نفس سطر الإدخال الرئيسي.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

### أمثلة

يوضح كيفية العمل مع الإدخالات الفرعية في حقل INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سيقوم إدخال INDEX بجمع كافة حقول XE ذات القيم المطابقة في خاصية "النص".
// في إدخال واحد بدلاً من عمل إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// حقول XE التي تحتوي على خاصية نص تصبح قيمتها عنوان إدخال INDEX.
// إذا كانت هذه القيمة تحتوي على جزأين من السلسلة مقسمتين بنقطتين (سيتعامل إدخال INDEX مع المحدد :)،
// الجزء الأول هو العنوان، والجزء الثاني سيصبح العنوان الفرعي.
// يقوم حقل INDEX أولاً بتجميع الإدخالات أبجديًا، ثم إذا كان هناك عدة حقول XE لها نفس الإدخال
// العناوين، سيقوم حقل INDEX بتجميعها فرعيًا حسب قيم هذه العناوين.
// يمكن أن تكون هناك طبقات تجميع فرعية متعددة، اعتمادًا على عدد المرات
// يتم تقسيم خصائص النص لحقول XE بهذا الشكل.
// بشكل افتراضي، ستقوم مجموعة إدخال حقل INDEX بإنشاء سطر جديد لكل عنوان فرعي داخل هذه المجموعة.
// يمكننا ضبط علامة RunSubentriesOnSameLine على القيمة true للاحتفاظ بالعنوان،
// وكل عنوان فرعي للمجموعة في سطر واحد بدلاً من ذلك، مما سيجعل حقل INDEX أكثر إحكاما.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// أدخل حقلي XE، كل منهما في صفحة جديدة، وبنفس العنوان المسمى "العنوان 1"،
// الذي سيستخدمه حقل INDEX لتجميعها.
// إذا كانت قيمة RunSubentriesOnSameLine خاطئة، فسيقوم جدول INDEX بإنشاء ثلاثة أسطر:
// سطر واحد لعنوان التجميع "العنوان 1"، وسطر آخر لكل عنوان فرعي.
// إذا كان RunSubentriesOnSameLine صحيحًا، فسيقوم جدول INDEX بإنشاء سطر واحد
// الإدخال الذي يشمل العنوان وكل عنوان فرعي.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldindex/)
* المجسم [Aspose.Words](../../../)


