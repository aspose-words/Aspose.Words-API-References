---
title: BorderCollection.Vertical
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection ملكية. يحصل على الحد العمودي المستخدم بين الخلايا.
type: docs
weight: 130
url: /ar/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

يحصل على الحد العمودي المستخدم بين الخلايا.

```csharp
public Border Vertical { get; }
```

### أمثلة

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


