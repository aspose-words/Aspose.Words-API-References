---
title: Table.Table
second_title: Aspose.Words لمراجع .NET API
description: Table البناء. يقوم بتهيئة مثيل جديد لملف الطاولة فئة .
type: docs
weight: 10
url: /ar/net/aspose.words.tables/table/table/
---
## Table constructor

يقوم بتهيئة مثيل جديد لملف **الطاولة** فئة .

```csharp
public Table(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

### ملاحظات

متي **الطاولة** تم إنشاؤه ، فهو ينتمي إلى المستند المحدد ، ولكنه ليس بعد جزءًا من المستند و **عقدة الأم** باطل.

لإلحاق **الطاولة** في المستند ، استخدم InsertAfter أو InsertBefore في المجموعة النصية حيث تريد إدراج الجدول.

### أمثلة

يوضح كيفية إنشاء جدول.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// تحتوي الجداول على صفوف تحتوي على خلايا قد تحتوي على فقرات
// مع عناصر نموذجية مثل المسارات والأشكال وحتى الجداول الأخرى.
// استدعاء طريقة "ضمان الحد الأدنى" على الطاولة سيضمن ذلك
// يحتوي الجدول على صف وخلية وفقرة واحدة على الأقل.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// أضف نصًا إلى المكالمة الأولى في الصف الأول من الجدول.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

يوضح كيفية إنشاء جدول متداخل بدون استخدام منشئ المستندات.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // أنشئ الجدول الخارجي بثلاثة صفوف وأربعة أعمدة ، ثم أضفه إلى المستند.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // أنشئ جدولًا آخر يحتوي على صفين وعمودين ثم أدخله في الخلية الأولى في الجدول الأول.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// ينشئ جدولًا جديدًا في المستند بالأبعاد المحددة والنص في كل خلية.
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

    // يمكنك استخدام خصائص "العنوان" و "الوصف" لإضافة عنوان ووصف على التوالي إلى جدولك.
    // يجب أن يحتوي الجدول على صف واحد على الأقل قبل أن نتمكن من استخدام هذه الخصائص.
    // هذه الخصائص مفيدة لمستندات .docx المتوافقة مع ISO / IEC 29500 (انظر فئة OoxmlCompliance).
    // إذا قمنا بحفظ المستند بتنسيقات ما قبل ISO / IEC 29500 ، فإن Microsoft Word يتجاهل هذه الخصائص.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### أنظر أيضا

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


