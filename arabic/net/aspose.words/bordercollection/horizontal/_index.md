---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BorderCollection الأفقية لحدود الخلايا والفقرات المتناسقة. حسّن تصميمك بمحاذاة وأسلوب مثاليين!
type: docs
weight: 50
url: /ar/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

يحصل على الحدود الأفقية المستخدمة بين الخلايا أو الفقرات المتوافقة.

```csharp
public Border Horizontal { get; }
```

## أمثلة

يوضح كيفية تطبيق الإعدادات على الحدود الأفقية لتنسيق الفقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ حدودًا أفقية حمراء للفقرة. أي فقرات تُنشأ بعد ذلك سترث إعدادات الحدود هذه.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// اكتب نصًا في المستند دون إنشاء فقرة جديدة بعد ذلك.
// نظرًا لعدم وجود فقرة أسفلها، فلن يكون الحد الأفقي مرئيًا.
builder.Write("Paragraph above horizontal border.");

// بمجرد أن نضيف فقرة ثانية، ستصبح حدود الفقرة الأولى مرئية.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

يوضح كيفية تطبيق الإعدادات على الحدود الرأسية لتنسيق صف الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء جدول بحدود داخلية باللونين الأحمر والأزرق.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    //ضبط مظهر الحدود التي ستظهر بين الصفوف.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    //ضبط مظهر الحدود التي ستظهر بين الخلايا.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
