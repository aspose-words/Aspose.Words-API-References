---
title: Enum HeightRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.HeightRule تعداد. يحدد قاعدة تحديد ارتفاع الكائن.
type: docs
weight: 3130
url: /ar/net/aspose.words/heightrule/
---
## HeightRule enumeration

يحدد قاعدة تحديد ارتفاع الكائن.

```csharp
public enum HeightRule
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| AtLeast | `0` | سيكون الارتفاع على الأقل الارتفاع المحدد بالنقاط. وسوف ينمو، إذا لزم الأمر، لاستيعاب كل النص داخل الكائن. |
| Exactly | `1` | الارتفاع محدد بالنقاط بالضبط. يرجى ملاحظة أنه إذا لم يكن من الممكن احتواء النص داخل الكائن بهذا الارتفاع، فسيظهر مقطوعًا. |
| Auto | `2` | سيزداد الارتفاع تلقائيًا لاستيعاب كل النص الموجود داخل الكائن. |

### أمثلة

يوضح كيفية تنسيق الصفوف باستخدام أداة إنشاء المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// ابدأ الصف الثاني، ثم قم بتكوين ارتفاعه. سيقوم المنشئ بتطبيق هذه الإعدادات على
// الصف الحالي، بالإضافة إلى أي صفوف جديدة يتم إنشاؤها بعد ذلك.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// لم يتأثر الصف الأول بإعادة تكوين الحشو ولا يزال يحتفظ بالقيم الافتراضية.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


