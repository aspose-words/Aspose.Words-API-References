---
title: HeaderFooter
second_title: Aspose.Words لمراجع .NET API
description: يمثل حاوية لنص رأس أو تذييل القسم.
type: docs
weight: 2920
url: /ar/net/aspose.words/headerfooter/
---
## HeaderFooter class

يمثل حاوية لنص رأس أو تذييل القسم.

```csharp
public class HeaderFooter : Story
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HeaderFooter](headerfooter)(DocumentBase, HeaderFooterType) | إنشاء رأس أو تذييل جديد من النوع المحدد. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstParagraph](../../aspose.words/story/firstparagraph) { get; } | الحصول على الفقرة الأولى في القصة . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype) { get; } | الحصول على نوع هذا الرأس / التذييل . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsHeader](../../aspose.words/headerfooter/isheader) { get; } | صحيح إذا كان هذا **تذييل الرأس** الكائن عبارة عن رأس . |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious) { get; set; } | صحيح إذا كان هذا الرأس أو التذييل مرتبطًا بالرأس أو التذييل المقابل_ x000d_ في القسم السابق. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [LastParagraph](../../aspose.words/story/lastparagraph) { get; } | الحصول على آخر فقرة في القصة . |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/headerfooter/nodetype) { get; } | عوائد **NodeType.HeaderFooter** . |
| [Paragraphs](../../aspose.words/story/paragraphs) { get; } | الحصول على مجموعة من الفقرات التي تمثل الأطفال المباشرين للقصة. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentSection](../../aspose.words/headerfooter/parentsection) { get; } | الحصول على القسم الأصل من هذه القصة . |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [StoryType](../../aspose.words/story/storytype) { get; } | الحصول على نوع هذه القصة . |
| [Tables](../../aspose.words/story/tables) { get; } | الحصول على مجموعة من الجداول التي تمثل الأطفال المباشرين للقصة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [AppendParagraph](../../aspose.words/story/appendparagraph)(string) | طريقة اختصار تنشئ ملف[`Paragraph`](../paragraph) كائن مع نص اختياري وإلحاقه بنهاية هذا الكائن. |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [DeleteShapes](../../aspose.words/story/deleteshapes)() | حذف كافة الأشكال من نص هذه القصة . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة ._ x000d_ |
| override [GetText](../../aspose.words/compositenode/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

**تذييل الرأس** يمكن أن تحتوي **فقرة** و **الطاولة** العقد الفرعية.

**تذييل الرأس** هي عقدة على مستوى القسم ويمكن أن تكون تابعة فقط لـ **الجزء** . يمكن أن يكون هناك واحد فقط **تذييل الرأس** أو كل منهما[`HeaderFooterType`](./headerfootertype) في **الجزء**.

إذا **الجزء** لا يملك **تذييل الرأس** من نوع معين or the **تذييل الرأس** لا يحتوي على عقد فرعية ، يعتبر هذا الرأس / التذييل مرتبطًا بـ رأس / تذييل الصفحة من نفس النوع من القسم السابق في Microsoft Word.

متي **تذييل الرأس** يحتوي على واحد على الأقل **فقرة**، لم يعد يتم اعتباره مرتبطًا بالسابق في Microsoft Word.

### أمثلة

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

يوضح كيفية حذف كل التذييلات من مستند.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// كرر خلال كل قسم وقم بإزالة التذييلات من كل نوع.
foreach (Section section in doc.OfType<Section>())
{
    // هناك ثلاثة أنواع من أنواع التذييل والرأس.
    // 1 - الرأس / التذييل "الأول" ، والذي يظهر فقط في الصفحة الأولى من القسم.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - الرأس / التذييل "الأساسي" ، والذي يظهر في الصفحات الفردية.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - رأس / تذييل "زوجي" ، والذي يظهر في الصفحات الزوجية.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// إنشاء رأس وإلحاق فقرة به. النص في تلك الفقرة
// في أعلى كل صفحة من هذا القسم ، فوق النص الأساسي الرئيسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// إنشاء تذييل وإلحاق فقرة به. النص في تلك الفقرة
// في أسفل كل صفحة من هذا القسم ، أسفل النص الأساسي الرئيسي.
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

* class [Story](../story)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
