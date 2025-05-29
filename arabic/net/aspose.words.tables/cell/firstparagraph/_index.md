---
title: Cell.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Cell FirstParagraph للوصول بسهولة إلى الفقرة الأولى من الأبناء المباشرين، مما يعزز إدارة المحتوى لديك.
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

يوضح كيفية إنشاء جدول متداخل باستخدام منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إنشاء الجدول الخارجي.
Cell cell = builder.InsertCell();
builder.Writeln("Outer Table Cell 1");
builder.InsertCell();
builder.Writeln("Outer Table Cell 2");
builder.EndTable();

//الانتقال إلى الخلية الأولى من الجدول الخارجي، ثم بناء جدول آخر داخل الخلية.
builder.MoveTo(cell.FirstParagraph);
builder.InsertCell();
builder.Writeln("Inner Table Cell 1");
builder.InsertCell();
builder.Writeln("Inner Table Cell 2");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertNestedTable.docx");
```

يوضح كيفية إنشاء جدول متداخل دون استخدام منشئ المستندات.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // قم بإنشاء الجدول الخارجي بثلاثة صفوف وأربعة أعمدة، ثم قم بإضافته إلى المستند.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // قم بإنشاء جدول آخر يحتوي على صفين وعمودين ثم أدخله في الخلية الأولى للجدول الأول.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// إنشاء جدول جديد في المستند بالأبعاد والنص المحددين في كل خلية.
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

    //يمكنك استخدام خصائص "العنوان" و"الوصف" لإضافة عنوان ووصف على التوالي إلى الجدول الخاص بك.
    // يجب أن يحتوي الجدول على صف واحد على الأقل قبل أن نتمكن من استخدام هذه الخصائص.
    // هذه الخصائص مفيدة للمستندات .docx المتوافقة مع ISO / IEC 29500 (انظر فئة OoxmlCompliance).
    // إذا قمنا بحفظ المستند بتنسيقات ما قبل ISO/IEC 29500، فإن Microsoft Word يتجاهل هذه الخصائص.
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
