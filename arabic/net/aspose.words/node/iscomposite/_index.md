---
title: Node.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words لـ .NET
description: Node IsComposite ملكية. إرجاعحقيقي إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى.

```csharp
public virtual bool IsComposite { get; }
```

### Property_Value

تعود هذه الطريقة`خطأ شنيع` مثل[`Node`](../) لا يمكن أن تحتوي على عقد فرعية.

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

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
