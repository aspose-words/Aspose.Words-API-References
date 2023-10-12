---
title: Comment.RemoveReply
second_title: Aspose.Words لمراجع .NET API
description: Comment طريقة. إزالة الرد المحدد على هذا التعليق.
type: docs
weight: 170
url: /ar/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

إزالة الرد المحدد على هذا التعليق.

```csharp
public void RemoveReply(Comment reply)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| reply | Comment | عقدة التعليق لحذف الرد. |

### ملاحظات

سيتم حذف كافة العقد المكونة للرد من المستند.

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

* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../comment/)
* المجسم [Aspose.Words](../../../)


