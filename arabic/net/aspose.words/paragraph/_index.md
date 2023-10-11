---
title: Class Paragraph
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Paragraph فصل. يمثل فقرة من النص.
type: docs
weight: 4390
url: /ar/net/aspose.words/paragraph/
---
## Paragraph class

يمثل فقرة من النص.

لمعرفة المزيد، قم بزيارة[العمل مع الفقرات](https://docs.aspose.com/words/net/working-with-paragraphs/) مقالة توثيقية.

```csharp
public class Paragraph : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | تهيئة مثيل جديد لـ`Paragraph` فئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | صحيح إذا كان فاصل الفقرة هذا عبارة عن فاصل نمط. يسمح فاصل الأنماط بأن تتكون فقرة one من أجزاء لها أنماط فقرات مختلفة. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | يوفر الوصول إلى خصائص تنسيق الإطار. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في أ[`Cell`](../../aspose.words.tables/cell/) ; كاذبة خلاف ذلك. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`HeaderFooter`](../headerfooter/) (قصة النص الرئيسي) من أ[`Section`](../section/) ; كاذبة خلاف ذلك. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`Body`](../body/) (قصة النص الرئيسي) من أ[`Section`](../section/) ; كاذبة خلاف ذلك. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | صحيح إذا كانت هذه الفقرة فرعًا مباشرًا لـ[`Cell`](../../aspose.words.tables/cell/) ; كاذبة خلاف ذلك. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | صحيح عندما تكون الفقرة عنصرًا في قائمة ذات تعداد نقطي أو رقمي في المراجعة الأصلية. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة الخاصة بالفقرة. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | يحصل على[`ListLabel`](./listlabel/)الكائن الذي يوفر الوصول إلى قيمة ترقيم القائمة وتنسيق لهذه الفقرة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | إرجاعParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف فاصل الفقرة. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | يوفر الوصول إلى خصائص تنسيق الفقرة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | يسترد الأصل[`Section`](../section/) من الفقرة. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | يسترد القصة على مستوى القسم الأصلي التي يمكن أن تكون[`Body`](../body/) أو[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | يوفر الوصول إلى مجموعة أجزاء النص المكتوبة داخل الفقرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | يقبل الزائر. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | إلحاق حقل بهذه الفقرة. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | إلحاق حقل بهذه الفقرة. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | إلحاق حقل بهذه الفقرة. |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | إرجاع مصفوفة من كافة علامات الجدولة المطبقة على هذه الفقرة، بما في ذلك المطبقة بشكل غير مباشر بواسطة الأنماط أو القوائم. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | الحصول على نص هذه الفقرة بما في ذلك حرف نهاية الفقرة. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | إدراج حقل في هذه الفقرة. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | إدراج حقل في هذه الفقرة. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | إدراج حقل في هذه الفقرة. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | يتم تشغيل عمليات الانضمام بنفس التنسيق في الفقرة. |
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

`Paragraph` هي عقدة على مستوى الكتلة ويمكن أن تكون فرعًا للفئات المشتقة من [`Story`](../story/) أو[`InlineStory`](../inlinestory/).

`Paragraph` يمكن أن تحتوي على أي عدد من العقد والإشارات المرجعية ذات المستوى المضمّن.

تتكون القائمة الكاملة للعقد الفرعية التي يمكن أن تحدث داخل الفقرة من [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/)[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/)[`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/)[`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/)[`Run`](../run/) ,[`SpecialChar`](../specialchar/)[`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/)[`SmartTag`](../../aspose.words.markup/smarttag/).

تنتهي الفقرة الصالحة في Microsoft Word دائمًا بحرف فاصل فقرة و وتتكون الفقرة الصحيحة الدنيا من فاصل فقرة فقط. ال`Paragraph` تقوم فئة تلقائيًا بإلحاق حرف فاصل الفقرة المناسب في end وهذا الحرف ليس جزءًا من العقد الفرعية لل`Paragraph` ، وبالتالي أ`Paragraph` يمكن أن تكون فارغة.

لا تقم بتضمين نهاية الفقرة[`ParagraphBreak`](../controlchar/paragraphbreak/) أو نهاية الخلية[`Cell`](../controlchar/cell/) الأحرف الموجودة داخل نص الفقرة لأنها قد تجعل الفقرة غير صالحة عند فتح المستند في Microsoft Word.

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

* class [CompositeNode](../compositenode/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


