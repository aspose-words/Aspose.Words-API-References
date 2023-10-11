---
title: Class Comment
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Comment فصل. يمثل حاوية لنص التعليق.
type: docs
weight: 230
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
| [Comment](comment/#constructor)(DocumentBase) | تهيئة مثيل جديد لـ`Comment` فئة. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | تهيئة مثيل جديد لـ`Comment` فئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | إرجاع الأصل`Comment` هدف. عائدات`باطل` للحصول على تعليقات عالية المستوى. |
| [Author](../../aspose.words/comment/author/) { get; set; } | إرجاع أو تعيين اسم المؤلف للتعليق. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | الحصول على تاريخ ووقت كتابة التعليق. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [Done](../../aspose.words/comment/done/) { get; set; } | الحصول على أو تعيين علامة تشير إلى أنه تم وضع علامة "تم" على التعليق. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | الحصول على الفقرة الأولى في القصة. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف الربط لهذا الكائن. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [Id](../../aspose.words/comment/id/) { get; set; } | الحصول على معرف التعليق. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | إرجاع أو تعيين الأحرف الأولى من اسم المستخدم المرتبط بتعليق معين. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | الحصول على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | إرجاعComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناء القصة مباشرة. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Replies](../../aspose.words/comment/replies/) { get; } | إرجاع مجموعة من`Comment` الكائنات التي تعتبر أبناء مباشرين للتعليق المحدد. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | إرجاعComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | يقبل الزائر. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(DocumentVisitor) |  |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | إضافة رد على هذا التعليق. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | إذا لم يكن العنصر الفرعي الأخير فقرة، فسيتم إنشاء فقرة واحدة فارغة وإلحاقها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | يزيل كافة الردود على هذا التعليق. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | إزالة الرد المحدد على هذا التعليق. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد الأول[`Node`](../node/) الذي يطابق تعبير XPath. |
| [SetText](../../aspose.words/comment/settext/)(string) | هذه طريقة ملائمة تتيح لك ضبط نص التعليق بسهولة. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

التعليق عبارة عن تعليق توضيحي يتم تثبيته على منطقة من النص أو على موضع في النص. يمكن أن يحتوي التعليق على قدر عشوائي من المحتوى على مستوى الكتلة.

اذا كان`Comment` يحدث الكائن من تلقاء نفسه، ويتم تثبيت التعليق على موضع الملف`Comment` هدف.

لربط تعليق بمنطقة نصية، يلزم وجود ثلاثة كائنات:`Comment`[`CommentRangeStart`](../commentrangestart/) و[`CommentRangeEnd`](../commentrangeend/) . تحتاج الكائنات الثلاثة إلى مشاركة نفس الشيء [`Id`](./id/) قيمة.

`Comment` هي عقدة ذات مستوى مضمّن ويمكن أن تكون فرعًا فقط لـ[`Paragraph`](../paragraph/).

`Comment` يمكن أن تحتوي[`Paragraph`](../paragraph/) و[`Table`](../../aspose.words.tables/table/) العقد الفرعية.

### أمثلة

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

* class [InlineStory](../inlinestory/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


