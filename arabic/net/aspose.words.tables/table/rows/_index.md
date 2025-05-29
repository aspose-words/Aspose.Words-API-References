---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى صفوف الجدول بسهولة باستخدام خصائصنا المكتوبة، مما يضمن إدارة سلسة للبيانات وتنظيمًا محسنًا لمشاريعك.
type: docs
weight: 260
url: /ar/net/aspose.words.tables/table/rows/
---
## Table.Rows property

يوفر الوصول المكتوب إلى صفوف الجدول.

```csharp
public RowCollection Rows { get; }
```

## أمثلة

يوضح كيفية دمج الصفوف من جدولين في جدول واحد.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// فيما يلي طريقتان للحصول على جدول من مستند.
// 1 - من مجموعة "الجداول" لعقدة الجسم:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - استخدام طريقة "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

//إضافة كافة الصفوف من الجدول الحالي إلى الجدول التالي.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// قم بإزالة حاوية الجدول الفارغة.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

يوضح كيفية تكرار جميع الجداول في المستند وطباعة محتويات كل خلية.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // يمكننا استخدام طريقة "ToArray" على مجموعة صفوف لاستنساخها في مصفوفة.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // يمكننا استخدام طريقة "ToArray" على مجموعة خلايا لاستنساخها في مصفوفة.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### أنظر أيضا

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
