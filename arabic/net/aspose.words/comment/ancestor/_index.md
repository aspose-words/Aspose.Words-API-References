---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words لـ .NET
description: Comment Ancestor ملكية. إرجاع الأصلComment هدف. عائداتباطل للحصول على تعليقات عالية المستوى في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

إرجاع الأصل[`Comment`](../) هدف. عائدات`باطل` للحصول على تعليقات عالية المستوى.

```csharp
public Comment Ancestor { get; }
```

## أمثلة

يوضح كيفية طباعة كافة تعليقات المستند والردود عليها.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// إذا لم يكن للتعليق أصل، فهو تعليق "المستوى الأعلى" وليس تعليقًا من نوع الرد.
// اطبع جميع التعليقات ذات المستوى الأعلى بالإضافة إلى أي ردود قد تكون لديهم.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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
