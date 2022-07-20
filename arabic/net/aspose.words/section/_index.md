---
title: Section
second_title: Aspose.Words لمراجع .NET API
description: يمثل قسمًا واحدًا في مستند.
type: docs
weight: 5440
url: /ar/net/aspose.words/section/
---
## Section class

يمثل قسمًا واحدًا في مستند.

```csharp
public sealed class Section : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Section](section)(DocumentBase) | تهيئة مثيل جديد لفئة القسم. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Body](../../aspose.words/section/body) { get; } | إرجاع ملف **الجسم** العقدة الفرعية للقسم. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| [HeadersFooters](../../aspose.words/section/headersfooters) { get; } | يوفر الوصول إلى رؤوس وتذييلات العقد الخاصة بالقسم. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/section/nodetype) { get; } | عوائد **نوع العقدة** . |
| [PageSetup](../../aspose.words/section/pagesetup) { get; } | إرجاع كائن يمثل إعداد الصفحة وخصائص القسم. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms) { get; set; } | صواب إذا كان القسم محميًا للنماذج. عندما يكون القسم محميًا للنماذج ، يمكن للمستخدمين تحديد النص وتعديله فقط في حقول النموذج في Microsoft Word . |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/section/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [AppendContent](../../aspose.words/section/appendcontent)(Section) | يتم إدراج نسخة من محتوى قسم المصدر في نهاية هذا القسم. |
| [ClearContent](../../aspose.words/section/clearcontent)() | مسح القسم. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters)() | مسح رؤوس وتذييلات هذا القسم. |
| [Clone](../../aspose.words/section/clone#clone_1)() | لإنشاء نسخة مكررة من هذا القسم. |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes)() | حذف كافة الأشكال (الكائنات الرسومية) من رؤوس وتذييلات هذا القسم ._ x000d_ |
| [EnsureMinimum](../../aspose.words/section/ensureminimum)() | يضمن أن القسم به نص فقرة واحدة. |
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
| [PrependContent](../../aspose.words/section/prependcontent)(Section) | يتم إدراج نسخة من محتوى قسم المصدر في بداية هذا القسم. |
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

**الجزء** يمكن أن يكون واحد[`Body`](./body) واحد كحد أقصى[`HeaderFooter`](../headerfooter) لكل منهما[`HeaderFooterType`](../headerfootertype) . **الجسم** و **تذييل الرأس** يمكن أن يكون nodes بأي ترتيب بالداخل **الجزء**.

الحد الأدنى من القسم الصالح يحتاج إلى **الجسم** مع واحد **فقرة**.

يحتوي كل قسم على مجموعة الخصائص الخاصة به التي تحدد حجم الصفحة والاتجاه والهوامش وما إلى ذلك.

يمكنك إنشاء نسخة من قسم باستخدام[`Clone`](../node/clone). يمكن إدراج النسخة في نفس المستند أو في مستند مختلف.

لإضافة أو إدراج أو إزالة قسم كامل بما في ذلك فاصل المقطع وخصائص القسم x000d_ استخدم طرق **الأقسام** هدف.

لنسخ وإدراج محتوى القسم فقط باستثناء المقطع break واستخدام خصائص القسم **AppendContent** و **PrependContent**طُرق.

### أمثلة

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد وجسم واحد وفقرة واحدة.
// اتصل بطريقة "RemoveAllChildren" لإزالة كل هذه العقد ،
// وتنتهي بعقدة مستند بدون توابع.
doc.RemoveAllChildren();

// لا يحتوي هذا المستند الآن على عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا كنا نرغب في تعديله ، فسنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً ، قم بإنشاء قسم جديد ، ثم قم بإلحاقه كعقدة فرعية بصفته فرعيًا.
Section section = new Section(doc);
doc.AppendChild(section);

// تعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى جسم يحتوي على جميع محتوياته ويعرضها
// في الصفحة الواقعة بين رأس وتذييل القسم.
Body body = new Body(doc);
section.AppendChild(body);

// قم بإنشاء فقرة ، وقم بتعيين بعض خصائص التنسيق ، ثم قم بإلحاقها كطفل بالجسم.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// أخيرًا ، أضف بعض المحتوى لعمل المستند. إنشاء شوط ،
// قم بتعيين مظهرها ومحتوياتها ، ثم قم بإلحاقها كطفل بالفقرة.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### أنظر أيضا

* class [CompositeNode](../compositenode)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
