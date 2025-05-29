---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Node NextPreOrder لاجتياز شجرة البيانات بكفاءة. تعلّم كيفية استرجاع العقدة التالية باستخدام خوارزمية الترتيب المسبق بفعالية!
type: docs
weight: 130
url: /ar/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق.

```csharp
public Node NextPreOrder(Node rootNode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| rootNode | Node | العقدة العلوية (الحد) للعبور. |

### قيمة الإرجاع

العقدة التالية في ترتيب الطلب المسبق. لا شيء إذا وصلت إلى*rootNode*.

## أمثلة

يوضح كيفية التنقل عبر شجرة عقد المستند باستخدام خوارزمية التنقل حسب الطلب، وحذف أي شكل يتم مواجهته مع صورة.

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
