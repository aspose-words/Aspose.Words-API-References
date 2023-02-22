---
title: SmartTag.NodeType
second_title: Aspose.Words لمراجع .NET API
description: SmartTag ملكية. عوائد NodeType.SmartTag .
type: docs
weight: 30
url: /ar/net/aspose.words.markup/smarttag/nodetype/
---
## SmartTag.NodeType property

عوائد **NodeType.SmartTag** .

```csharp
public override NodeType NodeType { get; }
```

### أمثلة

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [SmartTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../smarttag/)
* المجسم [Aspose.Words](../../../)


