---
title: Table.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table NodeType التي تقوم بإرجاع بيانات الجدول بكفاءة، مما يعزز إدارة البيانات وتنظيمها لتحقيق تكامل سلس.
type: docs
weight: 210
url: /ar/net/aspose.words.tables/table/nodetype/
---
## Table.NodeType property

إرجاعTable .

```csharp
public override NodeType NodeType { get; }
```

## أمثلة

يوضح كيفية التنقل عبر شجرة العقد المركبة من العقد الفرعية.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // أي عقدة يمكنها أن تحتوي على عقد فرعية، مثل المستند نفسه، هي عقدة مركبة.
    Assert.True(doc.IsComposite);

    // استدعاء الدالة التكرارية التي ستقوم بالمرور وطباعة جميع العقد الفرعية للعقدة المركبة.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// يتنقل بشكل متكرر عبر شجرة العقد أثناء طباعة نوع كل عقدة
/// مع مسافة بادئة تعتمد على العمق بالإضافة إلى محتويات جميع العقد المضمنة.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // كرر العملية في العقدة إذا كانت عقدة مركبة. وإلا، فاطبع محتوياتها إذا كانت عقدة مضمنة.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
