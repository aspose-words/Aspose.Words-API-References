---
title: Comment.Ancestor
second_title: Aspose.Words لمراجع .NET API
description: Comment ملكية. إرجاع كائن التعليق الأصل. إرجاع فارغ لتعليقات المستوى الأعلى.
type: docs
weight: 20
url: /ar/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

إرجاع كائن التعليق الأصل. إرجاع فارغ لتعليقات المستوى الأعلى.

```csharp
public Comment Ancestor { get; }
```

### أمثلة

يوضح كيفية طباعة كافة تعليقات المستند وردودهم.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// إذا لم يكن للتعليق أصل ، فهو تعليق من "المستوى الأعلى" بدلاً من تعليق من نوع الرد.
// طباعة جميع تعليقات المستوى الأعلى مع أي ردود قد تكون لديهم.
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
* مساحة الاسم [Aspose.Words](../../comment/)
* المجسم [Aspose.Words](../../../)


