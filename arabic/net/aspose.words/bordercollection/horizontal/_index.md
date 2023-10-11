---
title: BorderCollection.Horizontal
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection ملكية. يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المطابقة.
type: docs
weight: 50
url: /ar/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المطابقة.

```csharp
public Border Horizontal { get; }
```

### أمثلة

يوضح كيفية تطبيق الإعدادات على الحدود الأفقية على تنسيق الفقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حد أفقي أحمر للفقرة. أي فقرات تم إنشاؤها بعد ذلك سوف ترث إعدادات الحدود هذه.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// اكتب نصًا في المستند دون إنشاء فقرة جديدة بعد ذلك.
// نظرًا لعدم وجود فقرة أسفلها، لن يكون الحد الأفقي مرئيًا.
builder.Write("Paragraph above horizontal border.");

// بمجرد إضافة فقرة ثانية، ستصبح حدود الفقرة الأولى مرئية.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

يوضح كيفية تطبيق الإعدادات على الحدود الرأسية على تنسيق صف الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ جدولًا بحدود داخلية حمراء وزرقاء.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // اضبط مظهر الحدود التي ستظهر بين الصفوف.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // اضبط مظهر الحدود التي ستظهر بين الخلايا.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// يستخدم تنسيق الصف والفقرة الداخلية للخلية إعدادات حدود مختلفة.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### أنظر أيضا

* class [Border](../../border/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../bordercollection/)
* المجسم [Aspose.Words](../../../)


