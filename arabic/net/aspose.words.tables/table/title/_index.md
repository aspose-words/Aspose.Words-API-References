---
title: Table.Title
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على عنوان هذا الجدول أو تعيينه. يوفر تمثيلاً نصيًا بديلاً للمعلومات الموجودة في الجدول.
type: docs
weight: 320
url: /ar/net/aspose.words.tables/table/title/
---
## Table.Title property

الحصول على عنوان هذا الجدول أو تعيينه. يوفر تمثيلاً نصيًا بديلاً للمعلومات الموجودة في الجدول.

```csharp
public string Title { get; set; }
```

### ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

هذه الخاصية مفيدة لمستندات DOCX المتوافقة مع ISO/IEC 29500 ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). عند الحفظ بتنسيقات ما قبل ISO/IEC 29500، يتم تجاهل الخاصية.

### أمثلة

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

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


