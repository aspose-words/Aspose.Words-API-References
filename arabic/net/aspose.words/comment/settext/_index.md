---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words لـ .NET
description: Comment SetText طريقة. هذه طريقة ملائمة تتيح لك ضبط نص التعليق بسهولة في C#.
type: docs
weight: 150
url: /ar/net/aspose.words/comment/settext/
---
## Comment.SetText method

هذه طريقة ملائمة تتيح لك ضبط نص التعليق بسهولة.

```csharp
public void SetText(string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | النص الجديد للتعليق. |

## ملاحظات

تسمح هذه الطريقة بتعيين نص التعليق بسرعة من سلسلة. يمكن أن تحتوي السلسلة على فواصل فقرات، سيؤدي ذلك إلى إنشاء فقرات نصية في التعليق وفقًا لذلك. إذا كنت تريد إدراج عناصر أكثر تعقيدًا في التعليق، على سبيل المثال bookmarks أو الجداول أو تطبيق تنسيق منسق، فأنت بحاجة إلى استخدام فئات العقدة المناسبة إلى إنشاء نص التعليق.

## أمثلة

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
