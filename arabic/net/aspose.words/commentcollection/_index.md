---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.CommentCollection فصل. يوفر الوصول المكتوب إلى مجموعة منComment العقد في C#.
type: docs
weight: 240
url: /ar/net/aspose.words/commentcollection/
---
## CommentCollection class

يوفر الوصول المكتوب إلى مجموعة من[`Comment`](../comment/) العقد.

لمعرفة المزيد، قم بزيارة[العمل مع التعليقات](https://docs.aspose.com/words/net/working-with-comments/) مقالة توثيقية.

```csharp
public class CommentCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | يسترد أ[`Comment`](../comment/) في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | إضافة عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | إزالة كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | تحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | إدراج عقدة في المجموعة في الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | إزالة العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | نسخ كافة العقد من المجموعة إلى مجموعة جديدة من العقد. |

## أمثلة

يوضح كيفية وضع علامة "تم" على التعليق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // أدخل تعليقًا للإشارة إلى وجود خطأ.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // تحتوي التعليقات على علامة "تم"، والتي تم ضبطها على "خطأ" افتراضيًا.
// إذا كان هناك تعليق يشير إلى إجراء تغيير داخل المستند،
// يمكننا تطبيق التغيير، ثم تعيين علامة "تم" بعد ذلك للإشارة إلى التصحيح.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// التعليقات التي "تم" سوف تميز نفسها
// من تلك التي لم يتم "إتمامها" بلون نص باهت.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
