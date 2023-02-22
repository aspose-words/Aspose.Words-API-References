---
title: Row.Cells
second_title: Aspose.Words لمراجع .NET API
description: Row ملكية. يوفر وصولاً مكتوبًا إلى ملف خلية العقد الفرعية للصف .
type: docs
weight: 20
url: /ar/net/aspose.words.tables/row/cells/
---
## Row.Cells property

يوفر وصولاً مكتوبًا إلى ملف **خلية** العقد الفرعية للصف .

```csharp
public CellCollection Cells { get; }
```

### أمثلة

يوضح كيفية التكرار عبر جميع الجداول في المستند وطباعة محتويات كل خلية.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // يمكننا استخدام طريقة "ToArray" في مجموعة صف لاستنساخها في مصفوفة.
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

* class [CellCollection](../../cellcollection/)
* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../row/)
* المجسم [Aspose.Words](../../../)


