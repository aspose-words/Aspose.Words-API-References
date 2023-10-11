---
title: Node.NodeType
second_title: Aspose.Words لمراجع .NET API
description: Node ملكية. يحصل على نوع هذه العقدة.
type: docs
weight: 50
url: /ar/net/aspose.words/node/nodetype/
---
## Node.NodeType property

يحصل على نوع هذه العقدة.

```csharp
public abstract NodeType NodeType { get; }
```

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

يوضح كيفية إزالة جميع العقد الفرعية من نوع معين من العقدة المركبة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // احفظ العقدة الشقيقة التالية كمتغير في حالة أردنا الانتقال إليها بعد حذف هذه العقدة.
    Node nextNode = curNode.NextSibling;

    // يمكن أن يحتوي نص القسم على عقد الفقرة والجدول.
    // إذا كانت العقدة عبارة عن جدول، فقم بإزالتها من الأصل.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
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

* enum [NodeType](../../nodetype/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)


