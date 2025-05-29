---
title: Node.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Node IsComposite. حدّد بسهولة ما إذا كانت العقدة قادرة على استيعاب عقد أخرى، مما يُحسّن إدارة بنية بياناتك ومرونتها.
type: docs
weight: 30
url: /ar/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى.

```csharp
public virtual bool IsComposite { get; }
```

### Property_Value

هذه الطريقة تعيد`خطأ شنيع` مثل[`Node`](../) لا يمكن أن يكون لها عقد فرعية.

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

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
