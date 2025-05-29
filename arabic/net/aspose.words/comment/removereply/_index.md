---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words لـ .NET
description: أزل الردود غير المرغوب فيها بسهولة باستخدام خاصية "إزالة الردود من التعليقات"، مما يضمن وضوح مناقشاتك وفعاليتها. حسّن إدارة تعليقاتك اليوم!
type: docs
weight: 180
url: /ar/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

يزيل الرد المحدد على هذا التعليق.

```csharp
public void RemoveReply(Comment reply)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| reply | Comment | عقدة التعليق للرد المحذوف. |

## ملاحظات

سيتم حذف جميع العقد المكونة للرد من المستند.

## أمثلة

يوضح كيفية إزالة ردود التعليقات.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// فيما يلي طريقتان لإزالة الردود من التعليق.
// 1 - استخدم طريقة "RemoveReply" لإزالة الردود من تعليق فرديًا:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - استخدم طريقة "RemoveAllReplies" لإزالة جميع الردود من تعليق مرة واحدة:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### أنظر أيضا

* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
