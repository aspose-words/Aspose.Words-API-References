---
title: InlineStory Class
linktitle: InlineStory
articleTitle: InlineStory
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.InlineStory، القاعدة الأساسية للعقد المضمنة، والتي تتيح التكامل السلس للفقرات والجداول في مستنداتك.
type: docs
weight: 3720
url: /ar/net/aspose.words/inlinestory/
---
## InlineStory class

الفئة الأساسية للعقد ذات المستوى المضمن التي يمكن أن تحتوي على فقرات وجداول.

لمعرفة المزيد، قم بزيارة[المستويات المنطقية للعقد في المستند](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) مقالة توثيقية.

```csharp
public abstract class InlineStory : CompositeNode
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | يحصل على الفقرة الأولى في القصة. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف المرساة لهذا الكائن. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | يحصل على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | يحصل على نوع هذه العقدة. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناءً مباشرين للقصة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | يعيد نوع القصة. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | يحصل على مجموعة من الجداول التي تعتبر أبناءًا مباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | عند تنفيذه في فئة مشتقة، يتم استدعاء طريقة VisitXXXEnd للزائر المستند المحدد. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | عند تنفيذه في فئة مشتقة، يتم استدعاء طريقة VisitXXXStart للزائر المستند المحدد. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | إذا لم يكن الطفل الأخير فقرة، يتم إنشاء فقرة فارغة وإضافتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../node/) الذي يتطابق مع تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

`InlineStory` هو حاوية لعقد مستوى الكتلة[`Paragraph`](../paragraph/) و[`Table`](../../aspose.words.tables/table/).

الفئات التي تشتق من`InlineStory` هي عقد على مستوى السطر يمكنها أن تحتوي على نص خاص بها (فقرات وجداول). على سبيل المثال،[`Comment`](../comment/) تحتوي العقدة على نص تعليق و[`Footnote`](../../aspose.words.notes/footnote/) يحتوي على نص الحاشية السفلية.

## أمثلة

يوضح كيفية إضافة تعليق إلى فقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // في Microsoft Word، يمكننا النقر بزر الماوس الأيمن فوق هذا التعليق في نص المستند لتحريره أو الرد عليه.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستُضيف هذه الحاشية إشارة علوية صغيرة.
// ضع علامة بعد النص الذي تشير إليه وقم بإنشاء إدخال أسفل نص الهيئة الرئيسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على علامة مرجع الحاشية السفلية ونص المرجع،
// والتي سنمررها إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "true"، فسيتم استخدام علامة مرجع الحاشية السفلية لدينا
//سيكون فهرسها بين جميع حواشي القسم.
// هذه هي الحاشية الأولى، لذا فإن علامة المرجع ستكون "1".
Assert.True(footnote.IsAuto);

 // يمكننا نقل منشئ المستند داخل الحاشية السفلية لتحرير نص المرجع الخاص به.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة يستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// ستظل الإشارة المرجعية التي تم ضبط علم "IsAuto" عليها على "true" تعرض فهرسها الحقيقي
// حتى لو كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، فإن علامة مرجع هذه الإشارة المرجعية ستكون "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* class [CompositeNode](../compositenode/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
