---
title: CompositeNode.ChildNodes
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode ملكية. يحصل على جميع العقد الفرعية الفورية لهذه العقدة.
type: docs
weight: 10
url: /ar/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

يحصل على جميع العقد الفرعية الفورية لهذه العقدة.

```csharp
public NodeCollection ChildNodes { get; }
```

### ملاحظات

ملحوظة،`ChildNodes` يعادل الاتصال`GetChildNodes (NodeType.Any، false)` وإنشاء وإرجاع مجموعة جديدة في كل مرة يتم الوصول إليها.

في حالة عدم وجود عقد فرعية ، تقوم هذه الخاصية بإرجاع مجموعة فارغة.

### أمثلة

يوضح كيفية اجتياز مجموعة العقد المركبة الخاصة بالعقد الفرعية.

```csharp
Document doc = new Document();

// أضف شريطين وشكل واحد كعقد فرعية إلى الفقرة الأولى من هذا المستند.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن "CustomNodeId" لا يتم حفظه في ملف الإخراج ولا يوجد إلا أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// كرر من خلال مجموعة الفقرة للأطفال المباشرين ،
// وطباعة أي أشكال أو أشكال نجدها بالداخل.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### أنظر أيضا

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


