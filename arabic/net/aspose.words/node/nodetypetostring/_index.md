---
title: Node.NodeTypeToString
linktitle: NodeTypeToString
articleTitle: NodeTypeToString
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Node NodeTypeToString، وقم بتحويل أنواع العقد بسهولة إلى سلاسل سهلة الاستخدام للحصول على ترميز سلس وقابلية قراءة محسنة.
type: docs
weight: 170
url: /ar/net/aspose.words/node/nodetypetostring/
---
## Node.NodeTypeToString method

طريقة مساعدة تقوم بتحويل قيمة عددية لنوع العقدة إلى سلسلة سهلة الاستخدام.

```csharp
public static string NodeTypeToString(NodeType nodeType)
```

## أمثلة

يوضح كيفية استخدام خاصية NextSibling الخاصة بالعقدة لإجراء حصر من خلال أبنائها المباشرين.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

for (Node node = doc.FirstSection.Body.FirstChild; node != null; node = node.NextSibling)
{
    Console.WriteLine();
    Console.WriteLine($"Node type: {Node.NodeTypeToString(node.NodeType)}");

    string contents = node.GetText().Trim();
    Console.WriteLine(contents == string.Empty ? "This node contains no text" : $"Contents: \"{node.GetText().Trim()}\"");
}
```

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
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
