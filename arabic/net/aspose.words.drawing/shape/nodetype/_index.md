---
title: Shape.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: Shape NodeType ملكية. إرجاعShape  في C#.
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/shape/nodetype/
---
## Shape.NodeType property

إرجاعShape .

```csharp
public override NodeType NodeType { get; }
```

## أمثلة

يوضح كيفية اجتياز شجرة العقدة المركبة من العقد الفرعية.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // أي عقدة يمكن أن تحتوي على عقد فرعية، مثل المستند نفسه، تكون مركبة.
    Assert.True(doc.IsComposite);

    // استدعاء الوظيفة العودية التي ستمر عبر جميع العقد الفرعية للعقدة المركبة وتطبعها.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// يجتاز شجرة العقدة بشكل متكرر أثناء طباعة نوع كل عقدة
/// مع مسافة بادئة تعتمد على العمق بالإضافة إلى محتويات جميع العقد المضمنة.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // العودة إلى العقدة إذا كانت عقدة مركبة. بخلاف ذلك، قم بطباعة محتوياتها إذا كانت عقدة مضمنة.
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

### أنظر أيضا

* enum [NodeType](../../../aspose.words/nodetype/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
