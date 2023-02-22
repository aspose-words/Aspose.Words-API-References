---
title: TableCollection.ToArray
second_title: Aspose.Words لمراجع .NET API
description: TableCollection طريقة. نسخ كل الجداول من المجموعة إلى مصفوفة جداول جديدة.
type: docs
weight: 20
url: /ar/net/aspose.words.tables/tablecollection/toarray/
---
## TableCollection.ToArray method

نسخ كل الجداول من المجموعة إلى مصفوفة جداول جديدة.

```csharp
public Table[] ToArray()
```

### قيمة الإرجاع

صفيف من الجداول.

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

* class [Table](../../table/)
* class [TableCollection](../)
* مساحة الاسم [Aspose.Words.Tables](../../tablecollection/)
* المجسم [Aspose.Words](../../../)


