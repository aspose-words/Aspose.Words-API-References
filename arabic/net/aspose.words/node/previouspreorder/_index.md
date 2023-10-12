---
title: Node.PreviousPreOrder
second_title: Aspose.Words لمراجع .NET API
description: Node طريقة. الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق.
type: docs
weight: 140
url: /ar/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| rootNode | Node | العقدة العليا (الحد) للاجتياز. |

### قيمة الإرجاع

العقدة السابقة بترتيب مسبق. لاغية إذا وصلت إلى*rootNode*.

### أمثلة

يوضح كيفية اجتياز شجرة عقدة المستند باستخدام خوارزمية اجتياز الطلب المسبق، وحذف أي شكل يتم مواجهته مع الصورة.

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


