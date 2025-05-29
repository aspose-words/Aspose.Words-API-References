---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words لـ .NET
description: اكتشف ردود التعليقات. تمتع بالوصول إلى مجموعة من عناصر التعليقات التي تُعدّ ردودًا مباشرة على تعليقك المُحدد، مما يُعزز تفاعل المستخدمين.
type: docs
weight: 110
url: /ar/net/aspose.words/comment/replies/
---
## Comment.Replies property

يعيد مجموعة من[`Comment`](../) الكائنات التي تعتبر أبناءً مباشرين للتعليق المحدد.

```csharp
public CommentCollection Replies { get; }
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
