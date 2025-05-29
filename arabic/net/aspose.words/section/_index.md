---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Section، مفتاحك لإدارة أقسام المستندات الفردية بسهولة. حسّن تجربة تحرير مستنداتك اليوم!
type: docs
weight: 6560
url: /ar/net/aspose.words/section/
---
## Section class

يمثل قسمًا واحدًا في مستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public sealed class Section : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | يقوم بتهيئة مثيل جديد لفئة القسم. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | يعيد[`Body`](../body/) عقدة فرعية للقسم. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | يوفر الوصول إلى عقد الرؤوس والتذييلات الخاصة بالقسم. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | إرجاعSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | يعيد كائنًا يمثل إعداد الصفحة وخصائص القسم. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | صحيح إذا كان القسم محميًا للنماذج. عند حماية القسم للنماذج، يمكن للمستخدمين تحديد وتعديل النص فقط في حقول النموذج في مايكروسوفت وورد. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | يقوم بإدراج نسخة من محتوى قسم المصدر في نهاية هذا القسم. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | يمسح القسم. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters)() | مسح رؤوس وتذييلات هذا القسم. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters_1)(*bool*) | مسح رؤوس وتذييلات هذا القسم. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | ينشئ نسخة مكررة من هذا القسم. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | يحذف جميع الأشكال (كائنات الرسم) من رؤوس وتذييلات هذا القسم. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | يتأكد من أن القسم يحتوي على[`Body`](./body/) مع واحد[`Paragraph`](../paragraph/) . |
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
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | يقوم بإدراج نسخة من محتوى قسم المصدر في بداية هذا القسم. |
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

`Section` يمكن أن يكون له واحد[`Body`](../body/) والحد الأقصى واحد[`HeaderFooter`](../headerfooter/) لكل منهما[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) و[`HeaderFooter`](../headerfooter/) يمكن أن يكون nodes بأي ترتيب داخل`Section`.

يجب أن يحتوي القسم الصحيح على الحد الأدنى[`Body`](../body/) مع واحد[`Paragraph`](../paragraph/).

يحتوي كل قسم على مجموعة من الخصائص الخاصة به والتي تحدد حجم الصفحة والاتجاه والهوامش وما إلى ذلك.

يمكنك إنشاء نسخة من القسم باستخدام[`Clone`](../node/clone/)يمكن إدراج النسخة في نفس المستند أو مستند مختلف.

لإضافة أو إدراج أو إزالة قسم كامل بما في ذلك فاصل القسم وخصائص القسم x000d_، استخدم طرق[`Sections`](../document/sections/) هدف.

لنسخ وإدراج محتوى القسم فقط باستثناء break وخصائص القسم، استخدم[`AppendContent`](./appendcontent/) و[`PrependContent`](./prependcontent/) طُرق.

## أمثلة

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

//تحتوي الوثيقة الفارغة على قسم واحد ونص واحد وفقرة واحدة.
//استدعاء طريقة "RemoveAllChildren" لإزالة كل هذه العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا تحتوي هذه الوثيقة الآن على أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تحريره، فسوف نحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإضافته كقسم فرعي إلى عقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// تعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى نص، والذي سيحتوي على جميع محتوياته ويعرضها
// على الصفحة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// قم بإنشاء فقرة، ثم اضبط بعض خصائص التنسيق، ثم أضفها كفقرة فرعية إلى النص.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// أخيرًا، أضف بعض المحتوى لإنشاء المستند. أنشئ مسارًا،
// قم بتعيين مظهره ومحتوياته، ثم قم بإضافته كطفل إلى الفقرة.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### أنظر أيضا

* class [CompositeNode](../compositenode/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
