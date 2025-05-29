---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة SetText، وهي أداة سهلة الاستخدام تعمل على تبسيط إضافة التعليقات وتحسين سير عملك وتعزيز الإنتاجية دون عناء.
type: docs
weight: 190
url: /ar/net/aspose.words/comment/settext/
---
## Comment.SetText method

هذه طريقة ملائمة تسمح لك بتعيين نص التعليق بسهولة.

```csharp
public void SetText(string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | النص الجديد للتعليق. |

## ملاحظات

تتيح هذه الطريقة ضبط نص التعليق بسرعة من سلسلة نصية. يمكن أن تحتوي السلسلة على فواصل فقرات x000d_، مما يؤدي إلى إنشاء فقرات نصية في التعليق وفقًا لذلك. x000d_ إذا كنت ترغب في إدراج عناصر أكثر تعقيدًا في التعليق، مثل الإشارات المرجعية x000d_ أو الجداول، أو تطبيق تنسيق غني، فعليك استخدام فئات العقد المناسبة لإنشاء نص التعليق.

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
