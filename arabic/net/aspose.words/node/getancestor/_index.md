---
title: GetAncestor
second_title: Aspose.Words لمراجع .NET API
description: الحصول على الأصل الأول لنوع الكائن المحدد.
type: docs
weight: 110
url: /ar/net/aspose.words/node/getancestor/
---
## GetAncestor(Type) {#getancestor_1}

الحصول على الأصل الأول لنوع الكائن المحدد.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ancestorType | Type | نوع كائن الأصل المطلوب استرداده. |

### قيمة الإرجاع

سلف من النوع المحدد أو لاغٍ إذا لم يتم العثور على سلف من هذا النوع.

### ملاحظات

يتطابق نوع الأصل إذا كان يساوي ancestorType أو مشتقًا من ancestorType.

### أمثلة

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

        // اكتشف ما إذا كان الجدول متداخلًا داخل جدول آخر ، وإذا كان الأمر كذلك ، فبأي عمق.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// لحساب المستوى الذي يتداخل فيه الجدول داخل جداول أخرى.
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
/// يحدد ما إذا كان الجدول يحتوي على أي جدول تابع مباشر داخل خلاياه.
/// لا تجتاز هذه الجداول بشكل متكرر للتحقق من وجود المزيد من الجداول.
/// </summary>
/// <returns>
/// يعود صحيحاً إذا احتوت خلية فرعية واحدة على الأقل على جدول.
/// ترجع خطأ إذا لم تكن هناك خلايا في الجدول تحتوي على جدول.
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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)

---

## GetAncestor(NodeType) {#getancestor}

يحصل على أول سلف محدد[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ancestorType | NodeType | نوع عقدة الأصل المطلوب استرداده. |

### قيمة الإرجاع

سلف من النوع المحدد أو لاغٍ إذا لم يتم العثور على سلف من هذا النوع.

### أمثلة

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

        // اكتشف ما إذا كان الجدول متداخلًا داخل جدول آخر ، وإذا كان الأمر كذلك ، فبأي عمق.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// لحساب المستوى الذي يتداخل فيه الجدول داخل جداول أخرى.
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
/// يحدد ما إذا كان الجدول يحتوي على أي جدول تابع مباشر داخل خلاياه.
/// لا تجتاز هذه الجداول بشكل متكرر للتحقق من وجود المزيد من الجداول.
/// </summary>
/// <returns>
/// يعود صحيحاً إذا احتوت خلية فرعية واحدة على الأقل على جدول.
/// ترجع خطأ إذا لم تكن هناك خلايا في الجدول تحتوي على جدول.
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

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
