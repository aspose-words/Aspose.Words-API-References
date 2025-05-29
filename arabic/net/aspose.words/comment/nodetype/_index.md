---
title: Comment.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Comment NodeType التي تقوم بإرجاع التعليقات بكفاءة، مما يعزز تجربة إدارة المحتوى لديك من خلال التكامل السلس.
type: docs
weight: 90
url: /ar/net/aspose.words/comment/nodetype/
---
## Comment.NodeType property

إرجاعComment .

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

### أنظر أيضا

* enum [NodeType](../../nodetype/)
* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
