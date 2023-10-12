---
title: Class Body
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Body فصل. يمثل حاوية للنص الرئيسي للقسم.
type: docs
weight: 30
url: /ar/net/aspose.words/body/
---
## Body class

يمثل حاوية للنص الرئيسي للقسم.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class Body : Story
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Body](body/)(DocumentBase) | تهيئة مثيل جديد لـ`Body` فئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | الحصول على الفقرة الأولى في القصة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | الحصول على الفقرة الأخيرة في القصة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | إرجاعBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | يحصل على مجموعة من الفقرات التي تعتبر أبناء القصة مباشرة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | للحصول على القسم الأصلي لهذه القصة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | احصل على نوع هذه القصة. |
| [Tables](../../aspose.words/story/tables/) { get; } | الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(DocumentVisitor) | يقبل الزائر. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | طريقة اختصار لإنشاء ملف[`Paragraph`](../paragraph/) كائن بنص اختياري وإلحاقه بنهاية هذا الكائن. |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | حذف جميع الأشكال من نص هذه القصة. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | إذا لم يكن العنصر الفرعي الأخير فقرة، فسيتم إنشاء فقرة واحدة فارغة وإلحاقها. |
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
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد الأول[`Node`](../node/) الذي يطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

`Body` يمكن أن تحتوي[`Paragraph`](../paragraph/) و[`طاولة`](../../aspose.words.tables/table/) العقد الفرعية.

`Body` هي عقدة على مستوى القسم ويمكن أن تكون فرعًا فقط لـ[`Section`](../section/) . يمكن أن يكون هناك واحد فقط`Body` في[`Section`](../section/).

الحد الأدنى صالح`Body` يجب أن تحتوي على واحد على الأقل[`Paragraph`](../paragraph/).

### أمثلة

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

* class [Story](../story/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


