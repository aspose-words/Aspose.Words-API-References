---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Comment، أداتك الأساسية لإدارة نصوص التعليقات في المستندات. حسّن سير عملك بتكامل سلس!
type: docs
weight: 420
url: /ar/net/aspose.words/comment/
---
## Comment class

يمثل حاوية لنص التعليق.

لمعرفة المزيد، قم بزيارة[العمل مع التعليقات](https://docs.aspose.com/words/net/working-with-comments/) مقالة توثيقية.

```csharp
public sealed class Comment : InlineStory
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | يقوم بتهيئة مثيل جديد لـ`Comment` الصف. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | يقوم بتهيئة مثيل جديد لـ`Comment` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | يعيد الأصل`Comment`الكائن. يعود`باطل` للحصول على تعليقات المستوى الأعلى. |
| [Author](../../aspose.words/comment/author/) { get; set; } | يعيد أو يعين اسم المؤلف للتعليق. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | يحصل على التاريخ والوقت الذي تم فيه تقديم التعليق. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | يحصل على تاريخ ووقت UTC الذي تم فيه تقديم التعليق. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [Done](../../aspose.words/comment/done/) { get; set; } | يحصل على أو يعين علامة تشير إلى أن التعليق تم وضع علامة عليه بأنه تم الانتهاء منه. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | يحصل على الفقرة الأولى في القصة. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف المرساة لهذا الكائن. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [Id](../../aspose.words/comment/id/) { get; set; } | يحصل على معرف التعليق أو يعينه. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | يعيد أو يعين الأحرف الأولى للمستخدم المرتبط بتعليق معين. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | يحصل على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | إرجاعComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناءً مباشرين للقصة. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | يحصل على معرف التعليق الرئيسي أو يعينه. قيمة`-1` يعني أن التعليق ليس له أصل. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [Replies](../../aspose.words/comment/replies/) { get; } | يعيد مجموعة من`Comment` الكائنات التي تعتبر أبناءً مباشرين للتعليق المحدد. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | إرجاعComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | يحصل على مجموعة من الجداول التي تعتبر أبناءًا مباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر لزيارة نهاية التعليق. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر لزيارة بداية التعليق. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | يضيف ردًا على هذا التعليق. |
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
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | يزيل جميع الردود على هذا التعليق. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | يزيل الرد المحدد على هذا التعليق. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../node/) الذي يتطابق مع تعبير XPath. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | هذه طريقة ملائمة تسمح لك بتعيين نص التعليق بسهولة. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

التعليق هو عبارة عن توضيح مرتبط بمنطقة من النص أو بموضع في النص. يمكن أن يحتوي التعليق على كمية عشوائية من المحتوى على مستوى الكتلة.

إذا كان`Comment` إذا حدث الكائن من تلقاء نفسه، يتم تثبيت التعليق على موضع x000d_`Comment` هدف.

لتثبيت تعليق على منطقة من النص، هناك حاجة إلى ثلاثة كائنات:`Comment` ، [`CommentRangeStart`](../commentrangestart/) و[`CommentRangeEnd`](../commentrangeend/) يجب أن تشترك جميع الكائنات الثلاثة في نفس [`Id`](./id/) قيمة.

`Comment` هي عقدة على مستوى الخط ولا يمكن أن تكون إلا طفلة لـ[`Paragraph`](../paragraph/).

`Comment` يمكن أن تحتوي على[`Paragraph`](../paragraph/) و[`Table`](../../aspose.words.tables/table/) العقد الفرعية.

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

* class [InlineStory](../inlinestory/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
