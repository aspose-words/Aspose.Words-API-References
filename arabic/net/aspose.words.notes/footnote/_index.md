---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Notes.Footnote، وهي الأداة الأساسية لإدارة الحواشي السفلية والختامية بكل سهولة ودقة في مستنداتك.
type: docs
weight: 4950
url: /ar/net/aspose.words.notes/footnote/
---
## Footnote class

يمثل حاوية لنص الحاشية السفلية أو الحاشية النهائية.

لمعرفة المزيد، قم بزيارة[العمل مع الحواشي السفلية والختامية](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) مقالة توثيقية.

```csharp
public class Footnote : InlineStory
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | يقوم بتهيئة مثيل لـ`Footnote` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ActualReferenceMark](../../aspose.words.notes/footnote/actualreferencemark/) { get; } | يحصل على النص الفعلي لعلامة المرجع المعروضة في المستند لهذه الحاشية السفلية. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | يحصل على الفقرة الأولى في القصة. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف المرساة لهذا الكائن. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | ترجع قيمة تحدد ما إذا كانت هذه حاشية سفلية أم حاشية ختامية. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | تحتوي على قيمة تحدد ما إذا كانت هذه حاشية سفلية مرقمة تلقائيًا أو حاشية سفلية مع علامة مرجعية مخصصة يحددها المستخدم. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | يحصل على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | إرجاعFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناءً مباشرين للقصة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | يحصل على/يعين علامة مرجعية مخصصة لاستخدامها في هذه الحاشية السفلية. القيمة الافتراضية هي**سلسلة فارغة** (Empty )، مما يعني أنه يتم استخدام الحواشي المرقمة تلقائيًا. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | إرجاعFootnotes أوEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | يحصل على مجموعة من الجداول التي تعتبر أبناءًا مباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر لزيارة نهاية الحاشية السفلية. |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة بداية الحاشية السفلية. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | إذا لم يكن الطفل الأخير فقرة، يتم إنشاء فقرة فارغة وإضافتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../../aspose.words/node/) الذي يتطابق مع تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

ال`Footnote` يتم استخدام الفئة لتمثيل الحواشي السفلية والختامية في مستند Word.

`Footnote` هي عقدة على مستوى الخط ولا يمكن أن تكون إلا طفلة لـ[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` يمكن أن تحتوي على[`Paragraph`](../../aspose.words/paragraph/) و[`Table`](../../aspose.words.tables/table/) العقد الفرعية.

## أمثلة

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

* class [InlineStory](../../aspose.words/inlinestory/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
