---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.CommentCollection للوصول بسهولة إلى عقد التعليق، مما يعزز تحرير المستندات والتعاون في مشاريعك.
type: docs
weight: 430
url: /ar/net/aspose.words/commentcollection/
---
## CommentCollection class

يوفر وصولاً مكتوبًا إلى مجموعة من[`Comment`](../comment/) العقد.

لمعرفة المزيد، قم بزيارة[العمل مع التعليقات](https://docs.aspose.com/words/net/working-with-comments/) مقالة توثيقية.

```csharp
public class CommentCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | يحصل على عدد العقد في المجموعة. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | يسترجع[`Comment`](../comment/) عند الفهرس المعطى. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | يعيد الفهرس المبني على الصفر للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | يقوم بإدراج عقدة في المجموعة عند الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | يزيل العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | نسخ جميع العقد من المجموعة إلى مجموعة جديدة من العقد. |

## أمثلة

يوضح كيفية وضع علامة "تم" على التعليق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 //أدرج تعليقًا للإشارة إلى خطأ.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // تحتوي التعليقات على علامة "تم"، والتي يتم تعيينها على "خطأ" بشكل افتراضي.
// إذا اقترح أحد التعليقات إجراء تغيير داخل المستند،
// يمكننا تطبيق التغيير، ثم أيضًا تعيين علامة "تم" بعد ذلك للإشارة إلى التصحيح.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// التعليقات التي تم "إتمامها" سوف تميز نفسها
// من تلك التي لم يتم "إنهائها" بلون نص باهت.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
