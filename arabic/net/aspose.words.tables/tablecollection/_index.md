---
title: TableCollection Class
linktitle: TableCollection
articleTitle: TableCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Tables.TableCollection فصل. يوفر الوصول المكتوب إلى مجموعة منTable العقد في C#.
type: docs
weight: 6360
url: /ar/net/aspose.words.tables/tablecollection/
---
## TableCollection class

يوفر الوصول المكتوب إلى مجموعة من[`Table`](../table/) العقد.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public class TableCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words.tables/tablecollection/item/) { get; } | يسترد أ[`Table`](../table/) في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | إضافة عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | إزالة كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | تحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | إدراج عقدة في المجموعة في الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | إزالة العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words.tables/tablecollection/toarray/#toarray_1)() | نسخ كافة الجداول من المجموعة إلى مجموعة جديدة من الجداول. (2 methods) |

## أمثلة

يوضح كيفية إزالة الصفين الأول والأخير من كافة الجداول في المستند.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

يوضح كيفية معرفة ما إذا كانت الجداول متداخلة.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // اكتشف ما إذا كانت أي خلايا في الجدول تحتوي على جداول أخرى كأطفال.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // اكتشف ما إذا كان الجدول متداخلاً داخل جدول آخر، وإذا كان الأمر كذلك، فبأي عمق.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// يحسب مستوى تداخل الجدول داخل الجداول الأخرى.
/// </summary>
/// <returns>
/// عدد صحيح يشير إلى عمق تداخل الجدول (عدد عقد الجدول الأصل).
/// </returns>
private static int GetNestedDepthOfTable(Table table)
{
    int depth = 0;
    Node parent = table.GetAncestor(table.NodeType);

    while (parent != null)
    {
        depth++;
        parent = parent.GetAncestor(typeof(Table));
    }

    return depth;
}

/// <summary>
/// تحديد ما إذا كان الجدول يحتوي على أي جدول فرعي مباشر داخل خلاياه.
/// لا تقم بالتنقل عبر تلك الجداول بشكل متكرر للتحقق من وجود جداول أخرى.
/// </summary>
/// <returns>
/// يُرجع صحيحًا إذا كانت هناك خلية فرعية واحدة على الأقل تحتوي على جدول.
/// يُرجع خطأ إذا لم تكن هناك خلايا في الجدول تحتوي على جدول.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows.OfType<Row>())
    {
        foreach (Cell Cell in row.Cells.OfType<Cell>())
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### أنظر أيضا

* class [NodeCollection](../../aspose.words/nodecollection/)
* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
