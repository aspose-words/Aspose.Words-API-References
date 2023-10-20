---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words لـ .NET
description: Comment Replies ملكية. إرجاع مجموعة منComment الكائنات التي تعتبر أبناء مباشرين للتعليق المحدد في C#.
type: docs
weight: 90
url: /ar/net/aspose.words/comment/replies/
---
## Comment.Replies property

إرجاع مجموعة من[`Comment`](../) الكائنات التي تعتبر أبناء مباشرين للتعليق المحدد.

```csharp
public CommentCollection Replies { get; }
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
