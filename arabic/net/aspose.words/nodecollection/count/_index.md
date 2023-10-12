---
title: NodeCollection.Count
second_title: Aspose.Words لمراجع .NET API
description: NodeCollection ملكية. الحصول على عدد العقد في المجموعة.
type: docs
weight: 10
url: /ar/net/aspose.words/nodecollection/count/
---
## NodeCollection.Count property

الحصول على عدد العقد في المجموعة.

```csharp
public int Count { get; }
```

### أمثلة

يوضح كيفية اجتياز مجموعة العقد الفرعية للعقدة المركبة.

```csharp
Document doc = new Document();

// أضف مسارين وشكلًا واحدًا كعقد فرعية إلى الفقرة الأولى من هذه الوثيقة.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن "CustomNodeId" لا يتم حفظه في ملف إخراج وهو موجود فقط أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// كرر من خلال مجموعة الفقرة من العناصر الفرعية المباشرة،
// وطباعة أي مسارات أو أشكال نجدها داخلها.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
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

* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../nodecollection/)
* المجسم [Aspose.Words](../../../)


