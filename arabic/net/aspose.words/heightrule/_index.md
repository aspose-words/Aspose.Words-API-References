---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words لـ .NET
description: اكتشف قاعدة بيانات Aspose.Words.HeightRule للتحكم الدقيق في ارتفاع الكائنات في المستندات. حسّن سير عملك مع هذه الميزة الأساسية!
type: docs
weight: 3560
url: /ar/net/aspose.words/heightrule/
---
## HeightRule enumeration

يحدد القاعدة لتحديد ارتفاع الكائن.

```csharp
public enum HeightRule
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| AtLeast | `0` | سيكون الارتفاع على الأقل الارتفاع المحدد بالنقاط. سيزداد، عند الحاجة، ليتسع لجميع النصوص داخل الكائن. |
| Exactly | `1` | الارتفاع مُحدد بدقة بالنقاط. يُرجى ملاحظة أنه إذا لم يكن النص مناسبًا لحجم الكائن بهذا الارتفاع، فسيظهر مُقتطعًا. |
| Auto | `2` | سيزداد الارتفاع تلقائيًا لاستيعاب كل النص الموجود داخل الكائن. |

## أمثلة

يوضح كيفية تنسيق الصفوف باستخدام منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// ابدأ صفًا ثانيًا، ثم اضبط ارتفاعه. سيُطبّق المُنشئ هذه الإعدادات على
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
