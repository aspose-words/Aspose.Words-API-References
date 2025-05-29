---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words لـ .NET
description: استرجع كائن التعليق الرئيسي باستخدام خاصية "الأسلاف". مثالي للتنقل بين سلاسل التعليقات وتعزيز تفاعل المستخدمين.
type: docs
weight: 20
url: /ar/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

يعيد الأصل[`Comment`](../)الكائن. يعود`باطل` للحصول على تعليقات المستوى الأعلى.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
