---
title: CompositeNode.FirstChild
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode ملكية. يحصل على الطفل الأول للعقدة.
type: docs
weight: 20
url: /ar/net/aspose.words/compositenode/firstchild/
---
## CompositeNode.FirstChild property

يحصل على الطفل الأول للعقدة.

```csharp
public Node FirstChild { get; }
```

### ملاحظات

إذا لم تكن هناك عقدة فرعية أولى، أ`باطل` تم إرجاعها.

### أمثلة

يوضح كيفية استخدام خاصية NextSibling الخاصة بالعقدة للتعداد من خلال أبنائها المباشرين.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


