---
title: Node.GetAncestor
linktitle: GetAncestor
articleTitle: GetAncestor
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Node GetAncestor لاسترداد السلف الأول لنوع كائن محدد بسهولة، مما يعزز كفاءة ودقة الترميز لديك.
type: docs
weight: 110
url: /ar/net/aspose.words/node/getancestor/
---
## GetAncestor(*Type*) {#getancestor_1}

يحصل على السلف الأول لنوع الكائن المحدد.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ancestorType | Type | نوع الكائن السلف الذي سيتم استرجاعه. |

### قيمة الإرجاع

سلف النوع المحدد أو`باطل` إذا لم يتم العثور على سلف من هذا النوع.

## ملاحظات

يتطابق نوع السلف إذا كان مساويًا لـ*ancestorType* أو مشتقة من*ancestorType*.

## أمثلة

يوضح كيفية معرفة ما إذا كانت الجداول متداخلة.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // اكتشف ما إذا كانت أي خلايا في الجدول تحتوي على جداول أخرى كخلايا فرعية.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // اكتشف ما إذا كان الجدول متداخلاً داخل جدول آخر، وإذا كان الأمر كذلك، فما هو العمق.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// يحسب مستوى الجدول المتداخل داخل الجداول الأخرى.
/// </summary>
/// <returns>
/// عدد صحيح يشير إلى عمق التعشيش للجدول (عدد عقد الجدول الرئيسي).
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
/// يحدد ما إذا كان الجدول يحتوي على أي جدول فرعي مباشر داخل خلاياه.
/// لا تقم بالمرور بشكل متكرر عبر هذه الجداول للتحقق من وجود جداول أخرى.
/// </summary>
/// <returns>
/// يعود صحيحًا إذا كانت هناك خلية فرعية واحدة على الأقل تحتوي على جدول.
/// يتم إرجاع القيمة false إذا لم تحتوي أي خلايا في الجدول على جدول.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## GetAncestor(*[NodeType](../../nodetype/)*) {#getancestor}

يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ancestorType | NodeType | نوع العقدة السلفية التي سيتم استرجاعها. |

### قيمة الإرجاع

سلف النوع المحدد أو`باطل` إذا لم يتم العثور على سلف من هذا النوع.

## أمثلة

يوضح كيفية معرفة ما إذا كانت الجداول متداخلة.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // اكتشف ما إذا كانت أي خلايا في الجدول تحتوي على جداول أخرى كخلايا فرعية.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // اكتشف ما إذا كان الجدول متداخلاً داخل جدول آخر، وإذا كان الأمر كذلك، فما هو العمق.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// يحسب مستوى الجدول المتداخل داخل الجداول الأخرى.
/// </summary>
/// <returns>
/// عدد صحيح يشير إلى عمق التعشيش للجدول (عدد عقد الجدول الرئيسي).
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
/// يحدد ما إذا كان الجدول يحتوي على أي جدول فرعي مباشر داخل خلاياه.
/// لا تقم بالمرور بشكل متكرر عبر هذه الجداول للتحقق من وجود جداول أخرى.
/// </summary>
/// <returns>
/// يعود صحيحًا إذا كانت هناك خلية فرعية واحدة على الأقل تحتوي على جدول.
/// يتم إرجاع القيمة false إذا لم تحتوي أي خلايا في الجدول على جدول.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
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

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
