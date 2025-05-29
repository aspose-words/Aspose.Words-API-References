---
title: TableCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words لـ .NET
description: قم بتحويل TableCollection إلى مصفوفة بسهولة باستخدام طريقة ToArray، مما يؤدي إلى تبسيط إدارة البيانات وتعزيز أداء تطبيقك.
type: docs
weight: 20
url: /ar/net/aspose.words.tables/tablecollection/toarray/
---
## TableCollection.ToArray method

نسخ جميع الجداول من المجموعة إلى مجموعة جديدة من الجداول.

```csharp
public Table[] ToArray()
```

### قيمة الإرجاع

مجموعة من الجداول.

## أمثلة

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

* class [Table](../../table/)
* class [TableCollection](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
