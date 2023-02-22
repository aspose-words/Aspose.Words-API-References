---
title: Node.PreviousPreOrder
second_title: Aspose.Words لمراجع .NET API
description: Node طريقة. الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق.
type: docs
weight: 140
url: /ar/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| rootNode | Node | العقدة العلوية (حد) الاجتياز. |

### قيمة الإرجاع

العقدة السابقة بالطلب المسبق. لاغية إذا وصلت إلى rootNode.

### أمثلة

يوضح كيفية اجتياز شجرة عقد المستند باستخدام خوارزمية اجتياز الطلب المسبق ، وحذف أي شكل مصادفة مع صورة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

Assert.AreEqual(9, 
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));

Node curNode = doc;
while (curNode != null)
{
    Node nextNode = curNode.NextPreOrder(doc);

    if (curNode.PreviousPreOrder(doc) != null && nextNode != null)
        Assert.AreEqual(curNode, nextNode.PreviousPreOrder(doc));

    if (curNode.NodeType == NodeType.Shape && ((Shape)curNode).HasImage)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0,
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));
```

### أنظر أيضا

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)


