---
title: CommentCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: CommentCollection ملكية. يسترد أComment في الفهرس المحدد.
type: docs
weight: 10
url: /ar/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

يسترد أ[`Comment`](../../comment/) في الفهرس المحدد.

```csharp
public Comment this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس في المجموعة. |

### ملاحظات

المؤشر قائم على الصفر.

الفهارس السالبة مسموح بها وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر الموجودة في القائمة، فسيُرجع هذا مرجعًا فارغًا.

إذا كان الفهرس سالبًا وقيمته المطلقة أكبر من عدد العناصر الموجودة في القائمة، فسيُرجع هذا مرجعًا فارغًا.

### أمثلة

يوضح كيفية إزالة ردود التعليقات.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// فيما يلي طريقتان لإزالة الردود من التعليق.
// 1 - استخدم طريقة "RemoveReply" لإزالة الردود من التعليق بشكل فردي:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - استخدم طريقة "RemoveAllReplies" لإزالة كافة الردود من التعليق مرة واحدة:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### أنظر أيضا

* class [Comment](../../comment/)
* class [CommentCollection](../)
* مساحة الاسم [Aspose.Words](../../commentcollection/)
* المجسم [Aspose.Words](../../../)


