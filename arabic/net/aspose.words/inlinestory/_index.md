---
title: InlineStory
second_title: Aspose.Words لمراجع .NET API
description: الفئة الأساسية للعقد ذات المستوى المضمن التي يمكن أن تحتوي على فقرات وجداول.
type: docs
weight: 3070
url: /ar/net/aspose.words/inlinestory/
---
## InlineStory class

الفئة الأساسية للعقد ذات المستوى المضمن التي يمكن أن تحتوي على فقرات وجداول.

```csharp
public abstract class InlineStory : CompositeNode
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count/) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | الحصول على الفقرة الأولى في القصة . |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط الخاص بحرف الارتساء لهذا الكائن. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | الحصول على آخر تابع للعقدة . |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | الحصول على آخر فقرة في القصة . |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | يحصل على نوع هذه العقدة . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | الحصول على مجموعة من الفقرات التي تمثل الأطفال المباشرين للقصة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | استرداد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | إرجاع نوع القصة. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | الحصول على مجموعة من الجداول التي تمثل الأطفال المباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | يقبل الزائر . |
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
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

**InlineStory** عبارة عن حاوية للعقد على مستوى الكتلة[`Paragraph`](../paragraph/) و[`Table`](../../aspose.words.tables/table/).

الفئات التي تنبثق منها **InlineStory** هي عقد مضمنة يمكن أن تحتوي على نصوص خاصة بها (فقرات وجداول). على سبيل المثال ، أ **تعليق** العقدة تحتوي على نص comment و a **هامش** يحتوي على نص حاشية سفلية.

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

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا ، وقم بالإشارة إليه بحاشية سفلية. ستضع هذه الحاشية السفلية مرجعًا صغيرًا مرتفعًا
// علامة بعد النص الذي يشير إليه وإنشاء إدخال أسفل النص الأساسي الرئيسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على العلامة المرجعية للحاشية السفلية والنص المرجعي ،
// التي سنمررها إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "true" ، فإن العلامة المرجعية للحاشية السفلية الخاصة بنا
// سيكون فهرسها بين جميع الحواشي السفلية للقسم.
// هذه هي الحاشية الأولى ، لذا فإن العلامة المرجعية ستكون "1".
Assert.True(footnote.IsAuto);

// يمكننا نقل منشئ المستند داخل الحاشية السفلية لتحرير نصه المرجعي. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة ستستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// ستظل الإشارة المرجعية مع تعيين علامة "IsAuto" على "صواب" تظهر فهرسها الحقيقي
// حتى إذا كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة ، فإن العلامة المرجعية لهذه الإشارة المرجعية ستكون "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* class [CompositeNode](../compositenode/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
