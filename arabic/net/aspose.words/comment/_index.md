---
title: Class Comment
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Comment فصل. يمثل حاوية لنص تعليق.
type: docs
weight: 220
url: /ar/net/aspose.words/comment/
---
## Comment class

يمثل حاوية لنص تعليق.

```csharp
public sealed class Comment : InlineStory
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | يقوم بتهيئة مثيل جديد لملف **تعليق** فئة . |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | يقوم بتهيئة مثيل جديد لملف **تعليق** فئة . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | إرجاع كائن التعليق الأصل. إرجاع فارغ لتعليقات المستوى الأعلى. |
| [Author](../../aspose.words/comment/author/) { get; set; } | إرجاع أو تعيين اسم المؤلف للتعليق. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count/) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | الحصول على تاريخ ووقت عمل التعليق. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [Done](../../aspose.words/comment/done/) { get; set; } | الحصول على أو تعيين إشارة تشير إلى أنه تم وضع علامة "تم" على التعليق . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | الحصول على الفقرة الأولى في القصة . |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط الخاص بحرف الارتساء لهذا الكائن. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| [Id](../../aspose.words/comment/id/) { get; } | الحصول على معرف التعليق. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | إرجاع أو تعيين الأحرف الأولى للمستخدم المرتبط بتعليق محدد. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | الحصول على آخر تابع للعقدة . |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | الحصول على آخر فقرة في القصة . |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | عوائد **NodeType.Comment** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | الحصول على مجموعة من الفقرات التي تمثل الأطفال المباشرين للقصة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | استرداد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Replies](../../aspose.words/comment/replies/) { get; } | إرجاع مجموعة من`Comment` الكائنات التي هي تابعة مباشرة للتعليق المحدد. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | عوائد **نوع القصة** . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | الحصول على مجموعة من الجداول التي تمثل الأطفال المباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | يقبل الزائر . |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | لإضافة رد على هذا التعليق. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | إذا لم يكن الطفل الأخير فقرة ، فسيتم إنشاء وإلحاق فقرة واحدة فارغة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة . |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | يزيل كافة الردود على هذا التعليق. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | إزالة الرد المحدد على هذا التعليق. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [SetText](../../aspose.words/comment/settext/)(string) | هذه طريقة ملائمة تسمح لك بتعيين نص التعليق بسهولة. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

التعليق هو تعليق توضيحي يتم ربطه بمنطقة من النص أو إلى موضع في النص. يمكن أن يحتوي التعليق على كمية عشوائية من محتوى مستوى الحظر.

اذا كان`Comment` يحدث من تلقاء نفسه ، يتم ربط التعليق بـ موضع`Comment` هدف.

لإرساء تعليق بمنطقة من النص ، يلزم وجود ثلاثة عناصر:`Comment` ، [`CommentRangeStart`](../commentrangestart/) و[`CommentRangeEnd`](../commentrangeend/) تحتاج جميع الكائنات الثلاثة إلى مشاركة نفس [`Id`](./id/) القيمة.

`Comment` هي عقدة ذات مستوى مضمن ويمكن أن تكون تابعة فقط لـ[`Paragraph`](../paragraph/).

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

// في Microsoft Word ، يمكننا النقر بزر الماوس الأيمن فوق هذا التعليق في نص المستند لتحريره أو الرد عليه. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

يوضح كيفية إضافة تعليق إلى مستند ، ثم الرد عليه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// ضع التعليق في عقدة في نص المستند.
// سيظهر هذا التعليق في موقع فقرته ،
// خارج هامش الجانب الأيمن للصفحة ، وبخط منقط يربطها بالفقرة الخاصة بها.
builder.CurrentParagraph.AppendChild(comment);

// أضف ردًا ، والذي سيظهر تحت التعليق الأصلي.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// التعليقات والردود كلاهما عقد تعليق.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// التعليقات التي لا ترد على التعليقات الأخرى هي "عالية المستوى". ليس لديهم تعليقات أسلاف.
Assert.Null(comment.Ancestor);

// تحتوي الردود على تعليق من مستوى أعلى من سلف.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### أنظر أيضا

* class [InlineStory](../inlinestory/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


