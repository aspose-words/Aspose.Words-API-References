---
title: RowCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words لـ .NET
description: RowCollection ToArray طريقة. نسخ كافة الصفوف من المجموعة إلى مجموعة جديدة من الصفوف في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.tables/rowcollection/toarray/
---
## RowCollection.ToArray method

نسخ كافة الصفوف من المجموعة إلى مجموعة جديدة من الصفوف.

```csharp
public Row[] ToArray()
```

### قيمة الإرجاع

مجموعة من الصفوف.

## أمثلة

يوضح كيفية التكرار عبر كافة الجداول في المستند وطباعة محتويات كل خلية.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // يمكننا استخدام طريقة "ToArray" في مجموعة صفوف لاستنساخها في مصفوفة.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // يمكننا استخدام طريقة "ToArray" في مجموعة خلايا لاستنساخها في مصفوفة.
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

* class [Row](../../row/)
* class [RowCollection](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
