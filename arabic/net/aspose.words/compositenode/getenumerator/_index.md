---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: استكشف طريقة CompositeNode GetEnumerator لتكرار سلس على العقد الفرعية. حسّن كفاءة ترميزك مع هذه الميزة الفعّالة!
type: docs
weight: 120
url: /ar/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## أمثلة

يوضح كيفية طباعة كافة تعليقات المستند وردودها.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// إذا لم يكن للتعليق سلف، فهو تعليق "على مستوى أعلى" وليس تعليق من نوع الرد.
// اطبع جميع التعليقات ذات المستوى الأعلى بالإضافة إلى أي ردود قد تكون لديهم.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
