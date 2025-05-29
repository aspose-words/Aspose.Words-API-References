---
title: RowCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى أي صف بسهولة باستخدام خاصية RowCollection Item. استرجع البيانات بسرعة من الفهرس المطلوب لإدارة بياناتك بسلاسة.
type: docs
weight: 10
url: /ar/net/aspose.words.tables/rowcollection/item/
---
## RowCollection indexer

يسترجع[`Row`](../../row/) عند الفهرس المعطى.

```csharp
public Row this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للمجموعة. |

## ملاحظات

المؤشر يعتمد على الصفر.

يُسمح بالمؤشرات السلبية وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فسوف يؤدي هذا إلى إرجاع مرجع فارغ.

إذا كان الفهرس سلبيًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فسيؤدي هذا إلى إرجاع مرجع فارغ.

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

* class [Row](../../row/)
* class [RowCollection](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
