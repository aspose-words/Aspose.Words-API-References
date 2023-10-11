---
title: Comment.AddReply
second_title: Aspose.Words لمراجع .NET API
description: Comment طريقة. إضافة رد على هذا التعليق.
type: docs
weight: 150
url: /ar/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

إضافة رد على هذا التعليق.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | اسم المؤلف للرد. |
| initial | String | الأحرف الأولى من اسم المؤلف للرد. |
| dateTime | DateTime | تاريخ ووقت الرد. |
| text | String | نص الرد . |

### قيمة الإرجاع

الذي تم إنشاؤه[`Comment`](../) عقدة للرد.

### ملاحظات

نظرًا لقيود MS Office الحالية، يُسمح بمستوى واحد فقط من الردود في المستند. استثناء من النوعInvalidOperationException سيتم رفعه إذا تم استدعاء هذه الطريقة على تعليق الرد الموجود.

### أمثلة

يوضح كيفية إضافة تعليق إلى مستند، ثم الرد عليه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// ضع التعليق على عقدة في نص المستند.
// سيظهر هذا التعليق في مكان فقرته،
// خارج الهامش الأيمن للصفحة، وبخط منقط يصلها بالفقرة الخاصة بها.
builder.CurrentParagraph.AppendChild(comment);

// أضف ردًا، والذي سيظهر أسفل التعليق الأصلي.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// التعليقات والردود كلاهما عقد تعليق.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// التعليقات التي لا ترد على التعليقات الأخرى هي "المستوى الأعلى". ليس لديهم تعليقات الأجداد.
Assert.Null(comment.Ancestor);

// الردود لها تعليق من المستوى الأعلى للأسلاف.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### أنظر أيضا

* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../comment/)
* المجسم [Aspose.Words](../../../)


