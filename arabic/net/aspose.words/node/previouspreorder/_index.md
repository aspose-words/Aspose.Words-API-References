---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Node PreviousPreOrder لاسترداد العقدة السابقة بكفاءة باستخدام خوارزمية عبور شجرة الترتيب المسبق لتحسين معالجة البيانات.
type: docs
weight: 140
url: /ar/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| rootNode | Node | العقدة العلوية (الحد) للعبور. |

### قيمة الإرجاع

العقدة السابقة في ترتيب الطلب المسبق. لا شيء إذا وصلت إلى*rootNode*.

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
