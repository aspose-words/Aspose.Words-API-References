---
title: CommentCollection
second_title: Aspose.Words لمراجع .NET API
description: يوفر وصولاً مكتوبًا إلى مجموعة منComment./comment العقد ._ x000d_
type: docs
weight: 230
url: /ar/net/aspose.words/commentcollection/
---
## CommentCollection class

يوفر وصولاً مكتوبًا إلى مجموعة من[`Comment`](../comment) العقد ._ x000d_

```csharp
public class CommentCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/commentcollection/item) { get; } | يسترجع أ **تعليق** في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add)(Node) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear)() | يزيل كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains)(Node) | لتحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof)(Node) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert)(int, Node) | إدراج عقدة في المجموعة بالفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove)(Node) | يزيل العقدة من المجموعة ومن الوثيقة. |
| [RemoveAt](../../aspose.words/nodecollection/removeat)(int) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/nodecollection/toarray)() | ينسخ كل العقد من المجموعة إلى مصفوفة جديدة من العقد. |

### أمثلة

يوضح كيفية وضع علامة "تم" على تعليق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

// أدخل تعليقًا للإشارة إلى وجود خطأ. 
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

// التعليقات لها علامة "تم" ، والتي يتم تعيينها على "خطأ" افتراضيًا. 
// إذا كان هناك تعليق يشير إلى أننا نجري تغييرًا داخل المستند ،
// يمكننا تطبيق التغيير ، ثم أيضًا تعيين علامة "تم" بعد ذلك للإشارة إلى التصحيح.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// التعليقات "المنفذة" ستميز نفسها
// من تلك التي لم يتم "إنجازها" بلون نص باهت.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### أنظر أيضا

* class [NodeCollection](../nodecollection)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->