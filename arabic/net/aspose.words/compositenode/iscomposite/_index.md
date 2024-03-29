---
title: CompositeNode.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words لـ .NET
description: CompositeNode IsComposite ملكية. إرجاعحقيقي لأن هذه العقدة يمكن أن تحتوي على عقد فرعية في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية.

```csharp
public override bool IsComposite { get; }
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

* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
