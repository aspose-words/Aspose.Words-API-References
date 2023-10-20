---
title: Cell.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words لـ .NET
description: Cell FirstParagraph ملكية. يحصل على الفقرة الأولى بين الأطفال المباشرين في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.tables/cell/firstparagraph/
---
## Cell.FirstParagraph property

يحصل على الفقرة الأولى بين الأطفال المباشرين.

```csharp
public Paragraph FirstParagraph { get; }
```

## أمثلة

يوضح كيفية إنشاء جدول متداخل باستخدام أداة إنشاء المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ الجدول الخارجي.
Cell cell = builder.InsertCell();
builder.Writeln("Outer Table Cell 1");
builder.InsertCell();
builder.Writeln("Outer Table Cell 2");
builder.EndTable();

// انتقل إلى الخلية الأولى من الجدول الخارجي، وقم ببناء جدول آخر داخل الخلية.
builder.MoveTo(cell.FirstParagraph);
builder.InsertCell();
builder.Writeln("Inner Table Cell 1");
builder.InsertCell();
builder.Writeln("Inner Table Cell 2");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertNestedTable.docx");
```

يوضح كيفية إنشاء جدول متداخل دون استخدام أداة إنشاء المستندات.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // أنشئ الجدول الخارجي بثلاثة صفوف وأربعة أعمدة، ثم أضفه إلى المستند.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // أنشئ جدولًا آخر يتكون من صفين وعمودين، ثم أدخله في الخلية الأولى للجدول الأول.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// إنشاء جدول جديد في المستند بالأبعاد والنص المحدد في كل خلية.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // يمكنك استخدام خصائص "العنوان" و"الوصف" لإضافة عنوان ووصف على التوالي إلى الجدول الخاص بك.
    // يجب أن يحتوي الجدول على صف واحد على الأقل قبل أن نتمكن من استخدام هذه الخصائص.
    // هذه الخصائص مفيدة لمستندات .docx المتوافقة مع ISO / IEC 29500 (راجع فئة OoxmlCompliance).
    // إذا قمنا بحفظ المستند بتنسيقات ما قبل ISO/IEC 29500، فسيتجاهل Microsoft Word هذه الخصائص.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### أنظر أيضا

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
