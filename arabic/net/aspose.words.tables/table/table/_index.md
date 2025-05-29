---
title: Table
linktitle: Table
articleTitle: Table
second_title: Aspose.Words لـ .NET
description: أنشئ جداول مخصصة بسهولة باستخدام مُنشئ الجداول السهل الاستخدام. أنشئ، خصّص، وحسّن عرض بياناتك في دقائق!
type: docs
weight: 10
url: /ar/net/aspose.words.tables/table/table/
---
## Table constructor

يقوم بتهيئة مثيل جديد لـ[`Table`](../) الصف.

```csharp
public Table(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

## ملاحظات

متى[`Table`](../) يتم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس جزءًا من المستند بعد[`ParentNode`](../../../aspose.words/node/parentnode/) يكون`باطل`.

لإضافة[`Table`](../) لاستخدام المستند[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) أو[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) على القصة التي تريد إدراج الجدول فيها.

## أمثلة

يوضح كيفية إنشاء جدول.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// تحتوي الجداول على صفوف تحتوي على خلايا، والتي قد تحتوي على فقرات
// مع العناصر النموذجية مثل التشغيلات والأشكال وحتى الجداول الأخرى.
// سيؤدي استدعاء طريقة "EnsureMinimum" على جدول إلى ضمان ذلك
//يحتوي الجدول على صف واحد وخلية وفقرة واحدة على الأقل.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

//أضف نصًا إلى الخلية الأولى في الصف الأول من الجدول.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
