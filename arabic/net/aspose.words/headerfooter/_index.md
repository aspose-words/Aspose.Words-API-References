---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.HeaderFooter، الحل الأمثل لإدارة رؤوس وتذييلات الأقسام بسهولة. حسّن تنسيق مستنداتك اليوم!
type: docs
weight: 3530
url: /ar/net/aspose.words/headerfooter/
---
## HeaderFooter class

يمثل حاوية لنص الرأس أو التذييل لقسم ما.

لمعرفة المزيد، قم بزيارة[العمل مع الرؤوس والتذييلات](https://docs.aspose.com/words/net/working-with-headers-and-footers/) مقالة توثيقية.

```csharp
public class HeaderFooter : Story
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HeaderFooter](headerfooter/)(*[DocumentBase](../documentbase/), [HeaderFooterType](../headerfootertype/)*) | ينشئ رأسًا أو تذييلًا جديدًا من النوع المحدد. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | يحصل على الفقرة الأولى في القصة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | يحصل على نوع هذا الرأس/التذييل. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | صحيح إذا كان هذا`HeaderFooter` الكائن هو header. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | صحيح إذا كان هذا الرأس أو التذييل مرتبطًا بالرأس أو التذييل المقابل في القسم السابق. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | يحصل على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | إرجاعHeaderFooter . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناءً مباشرين للقصة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | يحصل على القسم الرئيسي لهذه القصة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | يحصل على نوع هذه القصة. |
| [Tables](../../aspose.words/story/tables/) { get; } | يحصل على مجموعة من الجداول التي تعتبر أبناءًا مباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words/headerfooter/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا لزيارة نهاية الرأس. |
| override [AcceptStart](../../aspose.words/headerfooter/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا لزيارة بداية الرأس. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | طريقة اختصار لإنشاء[`Paragraph`](../paragraph/) كائن يحتوي على نص اختياري ويضيفه إلى نهاية هذا الكائن. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | يحذف جميع الأشكال من نص هذه القصة. |
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

`HeaderFooter` يمكن أن تحتوي على[`Paragraph`](../paragraph/) و[`طاولة`](../../aspose.words.tables/table/) العقد الفرعية.

`HeaderFooter` هي عقدة على مستوى القسم ولا يمكن أن تكون إلا فرعًا لـ[`Section`](../section/) . لا يمكن أن يكون هناك سوى واحد`HeaderFooter` من كل واحد[`HeaderFooterType`](./headerfootertype/) في[`Section`](../section/).

لو[`Section`](../section/) ليس لديه`HeaderFooter` من نوع معين أو `HeaderFooter` لا يوجد لديه أي عقد فرعية، ويعتبر هذا الرأس/التذييل مرتبطًا بـ الرأس/التذييل من نفس نوع القسم السابق في Microsoft Word.

متى`HeaderFooter` يحتوي على واحد على الأقل[`Paragraph`](../paragraph/)، لم يعد من الممكن اعتباره مرتبطًا بالسابق في Microsoft Word.

## أمثلة

يوضح كيفية استبدال النص في تذييل المستند.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

يوضح كيفية حذف كافة التذييلات من المستند.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// قم بالتكرار خلال كل قسم وإزالة التذييلات من كل نوع.
foreach (Section section in doc.OfType<Section>())
{
    // هناك ثلاثة أنواع من أنواع التذييل والرأس.
    // 1 - "الرأس/التذييل الأول"، والذي يظهر فقط في الصفحة الأولى من القسم.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - الرأس/التذييل "الأساسي"، والذي يظهر في الصفحات الفردية.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - رأس/تذييل "الزوجي"، والذي يظهر في الصفحات الزوجية.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// أنشئ رأسًا وأضف إليه فقرة. النص في تلك الفقرة
// سوف تظهر في أعلى كل صفحة من هذا القسم، فوق النص الرئيسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// أنشئ تذييلًا وأضف إليه فقرة. النص في تلك الفقرة
// سوف تظهر في أسفل كل صفحة من هذا القسم، أسفل النص الرئيسي.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### أنظر أيضا

* class [Story](../story/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
