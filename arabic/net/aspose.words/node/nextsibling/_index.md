---
title: Node.NextSibling
second_title: Aspose.Words لمراجع .NET API
description: Node ملكية. يحصل على العقدة التي تلي هذه العقدة مباشرة.
type: docs
weight: 40
url: /ar/net/aspose.words/node/nextsibling/
---
## Node.NextSibling property

يحصل على العقدة التي تلي هذه العقدة مباشرة.

```csharp
public Node NextSibling { get; }
```

### ملاحظات

في حالة عدم وجود عقدة تالية ، يتم إرجاع قيمة فارغة .

### أمثلة

يوضح كيفية استخدام خاصية NextSibling للعقدة للتعداد من خلال توابعها المباشرين.

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

يوضح كيفية اجتياز شجرة العقد المركبة الخاصة بالعقد الفرعية.

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // أي عقدة يمكن أن تحتوي على عقد فرعية ، مثل المستند نفسه ، تكون مركبة.
    Assert.True(doc.IsComposite);

    // استدعاء الدالة العودية التي ستمر خلال وطباعة جميع العقد الفرعية للعقدة المركبة.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// يجتاز بشكل متكرر شجرة عقدة أثناء طباعة نوع كل عقدة
/// مع مسافة بادئة اعتمادًا على العمق بالإضافة إلى محتويات جميع العقد المضمنة.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // تكرر في العقدة إذا كانت عقدة مركبة. بخلاف ذلك ، اطبع محتوياته إذا كانت عقدة مضمنة.
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

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)


