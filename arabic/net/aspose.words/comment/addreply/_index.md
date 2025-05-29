---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مناقشاتك باستخدام طريقة Comment AddReply—قم بإضافة ردود على التعليقات بسهولة وقم بتحسين التفاعل على منصتك!
type: docs
weight: 160
url: /ar/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

يضيف ردًا على هذا التعليق.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | اسم المؤلف للرد. |
| initial | String | المؤلف يضع الأحرف الأولى من اسمه للرد. |
| dateTime | DateTime | التاريخ والوقت للرد. |
| text | String | نص الرد. |

### قيمة الإرجاع

تم إنشاؤه[`Comment`](../) عقدة للرد.

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidOperationException | يتم الرمي إذا تم استدعاء هذه الطريقة على تعليق الرد الموجود. |

## ملاحظات

بسبب القيود الحالية في MS Office، يُسمح بمستوى واحد فقط من الردود في المستند.

## أمثلة

يوضح كيفية إضافة تعليق إلى مستند، ثم الرد عليه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// ضع التعليق في عقدة داخل نص المستند.
// سيظهر هذا التعليق في مكان فقرته،
// خارج الهامش الأيمن للصفحة، وبخط منقط يربطه بالفقرة الخاصة به.
builder.CurrentParagraph.AppendChild(comment);

//أضف ردًا، والذي سيظهر أسفل تعليقه الرئيسي.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// التعليقات والردود هي عبارة عن عقد تعليق.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

التعليقات التي لا ترد على تعليقات أخرى تُعتبر "تعليقات عالية المستوى"، ولا تحتوي على تعليقات سابقة.
Assert.Null(comment.Ancestor);

// تحتوي الردود على تعليق على المستوى الأعلى.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### أنظر أيضا

* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
