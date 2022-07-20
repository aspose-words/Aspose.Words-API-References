---
title: Paragraph
second_title: Aspose.Words لمراجع .NET API
description: يمثل فقرة من النص .
type: docs
weight: 4150
url: /ar/net/aspose.words/paragraph/
---
## Paragraph class

يمثل فقرة من النص .

```csharp
public class Paragraph : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Paragraph](paragraph)(DocumentBase) | يقوم بتهيئة مثيل جديد لملف **فقرة** فئة ._ x000d_ |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator) { get; } | صواب إذا كان فاصل الفقرة هذا عبارة عن فاصل نمط. يسمح فاصل الأنماط بفقرة واحدة لتتكون من أجزاء لها أنماط فقرة مختلفة. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [FrameFormat](../../aspose.words/paragraph/frameformat) { get; } | يوفر الوصول إلى خصائص تنسيق الفقرة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في ملف[`Cell`](../../aspose.words.tables/cell) ؛ خطأ بخلاف ذلك. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في ملف **تذييل الرأس** (قصة النص الرئيسي) من أ **الجزء** ؛ خطأ بخلاف ذلك. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في ملف **الجسم** (قصة النص الرئيسي) من أ **الجزء** ؛ خطأ بخلاف ذلك. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInCell](../../aspose.words/paragraph/isincell) { get; } | صحيح إذا كانت هذه الفقرة تابعة مباشرة لـ[`Cell`](../../aspose.words.tables/cell) ؛ خطأ بخلاف ذلك. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsListItem](../../aspose.words/paragraph/islistitem) { get; } | صحيح عندما تكون الفقرة عنصرًا في قائمة ذات تعداد نقطي أو رقمي في المراجعة الأصلية. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [ListFormat](../../aspose.words/paragraph/listformat) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة للفقرة. |
| [ListLabel](../../aspose.words/paragraph/listlabel) { get; } | يحصل على أ[`ListLabel`](./listlabel) الذي يوفر الوصول إلى قائمة قيم الترقيم والتنسيق_ x000d_ لهذه الفقرة. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/paragraph/nodetype) { get; } | عوائد **نوع العقدة** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont) { get; } | يوفر الوصول إلى تنسيق خط حرف فاصل الفقرة. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat) { get; } | يوفر الوصول إلى خصائص تنسيق الفقرة. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentSection](../../aspose.words/paragraph/parentsection) { get; } | استرداد الأصل[`Section`](../section) من الفقرة ._ x000d_ |
| [ParentStory](../../aspose.words/paragraph/parentstory) { get; } | استرداد القصة الأصلية على مستوى القسم التي يمكن أن تكون[`Body`](../body) أو[`HeaderFooter`](../headerfooter) . |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Runs](../../aspose.words/paragraph/runs) { get; } | يوفر الوصول إلى مجموعة أجزاء النص المكتوبة داخل الفقرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_1)(string) | لإلحاق حقل بهذه الفقرة ._ x000d_ |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield)(FieldType, bool) | لإلحاق حقل بهذه الفقرة ._ x000d_ |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_2)(string, string) | لإلحاق حقل بهذه الفقرة ._ x000d_ |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops)() | إرجاع مصفوفة لجميع علامات الجدولة المطبقة على هذه الفقرة ، بما في ذلك تطبيقها بشكل غير مباشر بواسطة الأنماط أو القوائم. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة ._ x000d_ |
| override [GetText](../../aspose.words/paragraph/gettext)() | يحصل على نص هذه الفقرة متضمنًا حرف نهاية الفقرة. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_1)(string, Node, bool) | إدراج حقل في هذه الفقرة ._ x000d_ |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield)(FieldType, bool, Node, bool) | إدراج حقل في هذه الفقرة ._ x000d_ |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_2)(string, string, Node, bool) | إدراج حقل في هذه الفقرة ._ x000d_ |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting)() | تعمل الصلات بنفس التنسيق في الفقرة. |
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

[`Paragraph`](../paragraph) هي عقدة على مستوى الكتلة ويمكن أن تكون تابعة للفئات المشتقة من [`Story`](../story) أو[`InlineStory`](../inlinestory).

[`Paragraph`](../paragraph) يمكن أن يحتوي على أي عدد من العقد والإشارات المرجعية المضمنة.

تتكون القائمة الكاملة للعقد الفرعية التي يمكن أن تحدث داخل فقرة من [`BookmarkStart`](../bookmarkstart) و[`BookmarkEnd`](../bookmarkend) ، [`FieldStart`](../../aspose.words.fields/fieldstart) و[`FieldSeparator`](../../aspose.words.fields/fieldseparator) ، [`FieldEnd`](../../aspose.words.fields/fieldend) و[`FormField`](../../aspose.words.fields/formfield) ، [`Comment`](../comment) و[`Footnote`](../../aspose.words.notes/footnote) ، [`Run`](../run) و[`SpecialChar`](../specialchar) ، [`Shape`](../../aspose.words.drawing/shape) و[`GroupShape`](../../aspose.words.drawing/groupshape) ، [`SmartTag`](../../aspose.words.markup/smarttag).

تنتهي الفقرة الصالحة في Microsoft Word دائمًا بحرف فاصل فقرات و_ x000d_ تتكون أدنى فقرة صالحة من فاصل فقرة فقط. ال **فقرة** تُلحق فئة تلقائيًا حرف فاصل الفقرة المناسب في end وهذا الحرف ليس جزءًا من العقد الفرعية لـ **فقرة** ، لذلك_ x000d_ أ **فقرة** يمكن أن تكون فارغة.

لا تقم بتضمين نهاية الفقرة[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak) أو نهاية الخلية[`ControlChar.Cell`](../controlchar/cell) أحرف داخل نص الفقرة لأنها قد تجعل الفقرة غير صالحة عند فتح المستند في Microsoft Word.

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
