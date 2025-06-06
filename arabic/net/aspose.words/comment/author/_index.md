---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words لـ .NET
description: إدارة مؤلفي التعليقات بسهولة باستخدام خاصية "مؤلف التعليق". يمكنك بسهولة إرجاع أسماء المؤلفين أو تعيينها لتعزيز تفاعل المستخدمين ووضوح المحتوى.
type: docs
weight: 30
url: /ar/net/aspose.words/comment/author/
---
## Comment.Author property

يعيد أو يعين اسم المؤلف للتعليق.

```csharp
public string Author { get; set; }
```

## ملاحظات

لا يمكن أن يكون`باطل`.

افتراضيًا، السلسلة فارغة.

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
