---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Section فصل. يمثل قسمًا واحدًا في المستند في C#.
type: docs
weight: 5730
url: /ar/net/aspose.words/section/
---
## Section class

يمثل قسمًا واحدًا في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public sealed class Section : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | تهيئة مثيل جديد لفئة القسم. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | إرجاع[`Body`](../body/) العقدة الفرعية للقسم. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | يوفر الوصول إلى عقد الرؤوس والتذييلات الخاصة بالقسم. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | إرجاعSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | إرجاع كائن يمثل إعداد الصفحة وخصائص القسم. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | صحيح إذا كان القسم محميًا للنماذج. عندما يكون القسم محميًا للنماذج، يمكن للمستخدمين تحديد النص وتعديله فقط في حقول النموذج في Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | إضافة العقدة المحددة إلى نهاية قائمة العقد التابعة لهذه العقدة. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | إدراج نسخة من محتوى القسم المصدر في نهاية هذا القسم. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | مسح القسم. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | مسح رؤوس وتذييلات هذا القسم. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | إنشاء نسخة مكررة من هذا القسم. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | حذف كافة الأشكال (الكائنات الرسومية) من رؤوس وتذييلات هذا القسم. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | التأكد من وجود القسم[`Body`](./body/) مع واحد[`Paragraph`](../paragraph/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | يقوم بإدراج العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | إضافة العقدة المحددة إلى بداية قائمة العقد التابعة لهذه العقدة. |
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | إدراج نسخة من محتوى القسم المصدر في بداية هذا القسم. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | إزالة العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | تحديد الأول[`Node`](../node/) الذي يطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

`Section` يمكن أن يكون واحدا[`Body`](../body/) والحد الأقصى واحد[`HeaderFooter`](../headerfooter/) لكل منهما[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) و[`HeaderFooter`](../headerfooter/) يمكن أن يكون العقد بأي ترتيب بالداخل`Section`.

يجب أن يكون هناك حد أدنى من القسم الصالح[`Body`](../body/) مع واحد[`Paragraph`](../paragraph/).

يحتوي كل قسم على مجموعة الخصائص الخاصة به التي تحدد حجم الصفحة واتجاهها والهوامش وما إلى ذلك.

يمكنك إنشاء نسخة من القسم باستخدام[`Clone`](../node/clone/). يمكن إدراج النسخة في نفس المستند أو مستند مختلف.

لإضافة قسم كامل أو إدراجه أو إزالته بما في ذلك فاصل القسم وخصائص القسم ، استخدم أساليب[`Sections`](../document/sections/) هدف.

لنسخ محتوى القسم وإدراجه فقط باستثناء القسم Break واستخدام خصائص القسم[`AppendContent`](./appendcontent/) و[`PrependContent`](./prependcontent/) طُرق.

## أمثلة

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد ونص واحد وفقرة واحدة.
// اتصل بالطريقة "RemoveAllChildren" لإزالة كل تلك العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا يحتوي هذا المستند الآن على عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديله، فسنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإلحاقه كفرع لعقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// قم بتعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى نص يحتوي على جميع محتوياته ويعرضها
// في الصفحة الواقعة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// أنشئ فقرة، وعيّن بعض خصائص التنسيق، ثم ألحقها كطفل فرعي بالنص.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// وأخيرًا، أضف بعض المحتوى لإجراء المستند. إنشاء تشغيل،
// اضبط مظهرها ومحتوياتها، ثم ألحقها كطفل للفقرة.
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
