---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Paragraph لإدارة فقرات النص وتنسيقها بسهولة، مما يعزز قدرات معالجة المستندات لديك.
type: docs
weight: 5120
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
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | يقوم بتهيئة مثيل جديد لـ`Paragraph` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | صحيح إذا كان فاصل الفقرة هذا فاصل أنماط. يسمح فاصل الأنماط للفقرة الواحدة بأن تتكون من أجزاء ذات أنماط فقرات مختلفة. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | يوفر الوصول إلى خصائص تنسيق الإطار. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`Cell`](../../aspose.words.tables/cell/) ؛ وإلا فسيكون خاطئًا. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`HeaderFooter`](../headerfooter/) (قصة النص الرئيسي) لـ[`Section`](../section/) ؛ وإلا فسيكون خاطئًا. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`Body`](../body/) (قصة النص الرئيسي) لـ[`Section`](../section/) ؛ وإلا فسيكون خاطئًا. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | يعود صحيحًا إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | صحيح إذا كانت هذه الفقرة طفلًا مباشرًا لـ[`Cell`](../../aspose.words.tables/cell/) ؛ وإلا فسيكون خاطئًا. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | صحيح عندما تكون الفقرة عنصرًا في قائمة نقطية أو مرقمة في المراجعة الأصلية. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة للفقرة. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | يحصل على[`ListLabel`](./listlabel/)الكائن الذي يوفر الوصول إلى قيمة ترقيم القائمة وتنسيقها لهذه الفقرة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | إرجاعParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | يوفر الوصول إلى تنسيق الخط لحرف فاصل الفقرة. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | يوفر الوصول إلى خصائص تنسيق الفقرة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | يسترد الأصل[`Section`](../section/) من الفقرة. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | يسترد القصة على مستوى القسم الرئيسي التي يمكن[`Body`](../body/) أو[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | يوفر الوصول إلى مجموعة النصوص المكتوبة داخل الفقرة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر لزيارة نهاية فقرة المستند. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر لزيارة بداية فقرة المستند. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | يضيف حقلًا إلى هذه الفقرة. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | يضيف حقلًا إلى هذه الفقرة. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | يضيف حقلًا إلى هذه الفقرة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | إرجاع مجموعة من جميع علامات التبويب المطبقة على هذه الفقرة، بما في ذلك تلك المطبقة بشكل غير مباشر بواسطة الأنماط أو القوائم. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | يحصل على نص هذه الفقرة بما في ذلك حرف نهاية الفقرة. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | يُدرج حقلاً في هذه الفقرة. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | يُدرج حقلاً في هذه الفقرة. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | يُدرج حقلاً في هذه الفقرة. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | ينضم إلى التشغيلات بنفس التنسيق في الفقرة. |
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

`Paragraph` هي عقدة على مستوى الكتلة ويمكن أن تكون طفلة للفئات المشتقة من [`Story`](../story/) أو[`InlineStory`](../inlinestory/).

`Paragraph` يمكن أن يحتوي على أي عدد من العقد والإشارات المرجعية على المستوى المضمن.

تتكون القائمة الكاملة للعقد الفرعية التي يمكن أن تظهر داخل فقرة من [`BookmarkStart`](../bookmarkstart/) ،[`BookmarkEnd`](../bookmarkend/) ، [`FieldStart`](../../aspose.words.fields/fieldstart/) ،[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ، [`FieldEnd`](../../aspose.words.fields/fieldend/) ،[`FormField`](../../aspose.words.fields/formfield/) ، [`Comment`](../comment/) ،[`Footnote`](../../aspose.words.notes/footnote/) ، [`Run`](../run/) ،[`SpecialChar`](../specialchar/) ، [`Shape`](../../aspose.words.drawing/shape/) ،[`GroupShape`](../../aspose.words.drawing/groupshape/) ، [`SmartTag`](../../aspose.words.markup/smarttag/).

تنتهي الفقرة الصحيحة في Microsoft Word دائمًا بفاصل فقرة، وتتكون الفقرة الصحيحة الدنيا من فاصل فقرة فقط.`Paragraph` تضيف فئة تلقائيًا حرف فاصل الفقرة المناسب في نهاية وهذا الحرف ليس جزءًا من العقد الفرعية لـ`Paragraph` ، لذلك أ`Paragraph` يمكن أن تكون فارغة.

لا تتضمن نهاية الفقرة[`ParagraphBreak`](../controlchar/paragraphbreak/) أو نهاية الخلية[`Cell`](../controlchar/cell/) الأحرف الموجودة داخل نص الفقرة حيث قد يؤدي ذلك إلى جعل الفقرة غير صالحة عند فتح المستند في Microsoft Word.

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
