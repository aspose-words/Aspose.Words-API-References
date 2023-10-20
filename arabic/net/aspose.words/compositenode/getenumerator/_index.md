---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: CompositeNode GetEnumerator طريقة. يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## أمثلة

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

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
