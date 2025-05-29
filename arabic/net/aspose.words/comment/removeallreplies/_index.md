---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words لـ .NET
description: قم بمسح جميع الردود على تعليقك بسهولة باستخدام طريقة RemoveAllReplies، مما يضمن مناقشة خالية من الفوضى وتجربة مستخدم محسنة.
type: docs
weight: 170
url: /ar/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

يزيل جميع الردود على هذا التعليق.

```csharp
public void RemoveAllReplies()
```

## ملاحظات

سيتم حذف جميع العقد المكونة للردود من المستند.

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
