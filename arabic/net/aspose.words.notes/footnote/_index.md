---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Notes.Footnote فصل. يمثل حاوية لنص الحاشية السفلية أو التعليق الختامي في C#.
type: docs
weight: 4260
url: /ar/net/aspose.words.notes/footnote/
---
## Footnote class

يمثل حاوية لنص الحاشية السفلية أو التعليق الختامي.

لمعرفة المزيد، قم بزيارة[العمل مع الحواشي السفلية والتعليقات الختامية](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) مقالة توثيقية.

```csharp
public class Footnote : InlineStory
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | تهيئة مثيل لـ`Footnote` فئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | الحصول على الفقرة الأولى في القصة. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف الربط لهذا الكائن. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | تُرجع قيمة تحدد ما إذا كانت هذه حاشية سفلية أم تعليق ختامي. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | يحمل قيمة تحدد ما إذا كانت هذه حاشية سفلية مرقمة تلقائيًا أو حاشية سفلية بعلامة مرجعية مخصصة يحددها المستخدم. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | الحصول على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | إرجاعFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناء القصة مباشرة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | الحصول على/تعيين علامة مرجعية مخصصة لاستخدامها في هذه الحاشية السفلية. القيمة الافتراضية هي**سلسلة فارغة** (Empty )، مما يعني استخدام الحواشي السفلية المرقمة تلقائيًا. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | إرجاعFootnotes أوEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | إضافة العقدة المحددة إلى نهاية قائمة العقد التابعة لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | إذا لم يكن العنصر الفرعي الأخير فقرة، فسيتم إنشاء فقرة واحدة فارغة وإلحاقها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | إضافة العقدة المحددة إلى بداية قائمة العقد التابعة لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | إزالة العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | تحديد الأول[`Node`](../../aspose.words/node/) الذي يطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

ال`Footnote` يتم استخدام الفئة لتمثيل الحواشي السفلية والتعليقات الختامية في مستند Word.

`Footnote` هي عقدة ذات مستوى مضمّن ويمكن أن تكون فرعًا فقط لـ[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` يمكن أن تحتوي[`Paragraph`](../../aspose.words/paragraph/) و[`Table`](../../aspose.words.tables/table/) العقد الفرعية.

## أمثلة

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستضع هذه الحاشية السفلية مرجعًا مرتفعًا صغيرًا
// ضع علامة بعد النص الذي تشير إليه وقم بإنشاء إدخال أسفل النص الأساسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على العلامة المرجعية للحاشية السفلية والنص المرجعي،
// والذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "صحيح"، فستكون العلامة المرجعية للحاشية السفلية
// سيكون فهرسه بين جميع الحواشي السفلية للقسم.
// هذه هي الحاشية السفلية الأولى، لذا ستكون العلامة المرجعية "1".
Assert.True(footnote.IsAuto);

 // يمكننا نقل أداة إنشاء المستندات داخل الحاشية السفلية لتحرير النص المرجعي الخاص بها.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة تستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// الإشارة المرجعية التي تم ضبط علامة "IsAuto" على "صحيح" ستظل تُظهر فهرسها الحقيقي
// حتى لو كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، فستكون العلامة المرجعية لهذه الإشارة المرجعية "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* class [InlineStory](../../aspose.words/inlinestory/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
