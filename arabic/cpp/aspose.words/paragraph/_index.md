---
title: "فئة Aspose::Words::Paragraph"
linktitle: "Paragraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Paragraph. تمثل فقرة نصية. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 47000
url: /ar/cpp/aspose.words/paragraph/
---
## Paragraph class


يمثل فقرة نصية. لمعرفة المزيد، زر مقالة الوثائق [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية فقرة المستند. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية فقرة المستند. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | يضيف حقلًا إلى هذه الفقرة. |
| [AppendField](./appendfield/)(const System::String\&) | يضيف حقلًا إلى هذه الفقرة. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | يضيف حقلًا إلى هذه الفقرة. |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | صحيح إذا كان فاصل الفقرة هذا هو [Style](../style/) Separator. يسمح فاصل النمط لفقرة واحدة بأن تتكون من أجزاء ذات أنماط فقرة مختلفة. |
| [get_Count](../compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FrameFormat](./get_frameformat/)() | يوفر الوصول إلى خصائص تنسيق الإطار. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsEndOfCell](./get_isendofcell/)() | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في [Cell](../../aspose.words.tables/cell/); خطأ غير ذلك. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في [HeaderFooter](../headerfooter/) (قصة النص الرئيسي) لقسم [Section](../section/); خطأ غير ذلك. |
| [get_IsEndOfSection](./get_isendofsection/)() | صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في [Body](../body/) (قصة النص الرئيسي) لقسم [Section](../section/); خطأ غير ذلك. |
| [get_IsFormatRevision](./get_isformatrevision/)() | يرجع true إذا تم تغيير تنسيق الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsInCell](./get_isincell/)() | صحيح إذا كانت هذه الفقرة طفلاً مباشرًا لـ [Cell](../../aspose.words.tables/cell/); خطأ غير ذلك. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsListItem](./get_islistitem/)() | صحيح عندما تكون الفقرة عنصرًا في قائمة نقطية أو مرقمة في المراجعة الأصلية. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_LastChild](../compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_ListFormat](./get_listformat/)() | يوفر الوصول إلى خصائص تنسيق القائمة للفقرة. |
| [get_ListLabel](./get_listlabel/)() | يحصل على كائن [ListLabel](./get_listlabel/) يوفر الوصول إلى قيمة ترقيم القائمة وتنسيقها لهذه الفقرة. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [Paragraph](../nodetype/). |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | يوفر الوصول إلى تنسيق الخط لحرف فاصل الفقرة. |
| [get_ParagraphFormat](./get_paragraphformat/)() | يوفر الوصول إلى خصائص تنسيق الفقرة. |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentSection](./get_parentsection/)() | يسترجع الـ[Section](../section/) الأب للفقرة. |
| [get_ParentStory](./get_parentstory/)() | يسترجع القصة على مستوى القسم الأب التي يمكن أن تكون [Body](../body/) أو [HeaderFooter](../headerfooter/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_Runs](./get_runs/)() | يوفر الوصول إلى مجموعة الأنواع من قطع النص داخل الفقرة. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | يرجع مصفوفة جميع نقاط التبويب المطبقة على هذه الفقرة، بما في ذلك تلك المطبقة بشكل غير مباشر عبر الأنماط أو القوائم. |
| [GetEnumerator](../compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetText](./gettext/)() override | يحصل على نص هذه الفقرة بما في ذلك حرف نهاية الفقرة. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يدرج حقلًا في هذه الفقرة. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يدرج حقلًا في هذه الفقرة. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يدرج حقلًا في هذه الفقرة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | يجمع المقاطع ذات التنسيق نفسه في الفقرة. |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | يجمع المقاطع ذات التنسيق نفسه في الفقرة. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | يُهيئ نسخة جديدة من الفئة [Paragraph](./). |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../node/remove/)() | يزيل نفسه من العنصر الأب. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](../../aspose.words.markup/smarttag/) للعقدة الحالية. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../node/) يطابق تعبير XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

القائمة الكاملة لعقد الأطفال التي يمكن أن تظهر داخل الفقرة تتكون من [BookmarkStart](../bookmarkstart/)، [BookmarkEnd](../bookmarkend/)، [FieldStart](../../aspose.words.fields/fieldstart/)، [FieldSeparator](../../aspose.words.fields/fieldseparator/)، [FieldEnd](../../aspose.words.fields/fieldend/)، [FormField](../../aspose.words.fields/formfield/)، [Comment](../comment/)، [Footnote](../../aspose.words.notes/footnote/)، [Run](../run/)، [SpecialChar](../specialchar/)، [Shape](../../aspose.words.drawing/shape/)، [GroupShape](../../aspose.words.drawing/groupshape/)، [SmartTag](../../aspose.words.markup/smarttag/).

الفقرة الصالحة في Microsoft Word تنتهي دائمًا بحرف فاصل الفقرة، والفقرة الصالحة الأدنى تتكون فقط من فاصل الفقرة. تقوم فئة [Paragraph](./) تلقائيًا بإضافة حرف فاصل الفقرة المناسب في النهاية، وهذا الحرف ليس جزءًا من عقد الأطفال في [Paragraph](./)، وبالتالي يمكن أن تكون [Paragraph](./) فارغة.

لا تُدرج أحرف نهاية الفقرة [ParagraphBreak](../controlchar/paragraphbreak/) أو نهاية الخلية [Cell](../controlchar/cell/) داخل نص الفقرة، فقد يؤدي ذلك إلى جعل الفقرة غير صالحة عند فتح المستند في Microsoft Word.

## أمثلة



يوضح كيفية إنشاء مستند Aspose.Words يدويًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يحتوي مستند فارغ على قسم واحد، جسم واحد وفقرة واحدة.
// استدعِ طريقة "RemoveAllChildren" لإزالة جميع تلك العقد،
// وانتهي إلى عقدة مستند بدون أي أبناء.
doc->RemoveAllChildren();

// ليس لهذا المستند الآن أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديلها، سنحتاج إلى إعادة ملء مجموعة العقد الخاصة بها.
// أولاً، أنشئ قسمًا جديدًا، ثم أضفه كطفل إلى عقدة المستند الجذرية.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// حدد بعض خصائص إعداد الصفحة للقسم.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// يحتاج القسم إلى جسم، سيحتوي ويعرض جميع محتوياته
// على الصفحة بين رأس وتذييل القسم.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// أنشئ فقرة، واضبط بعض خصائص التنسيق، ثم أضفها كعنصر فرعي إلى الجسم.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// أخيرًا، أضف بعض المحتوى لإنشاء المستند. أنشئ عنصر Run،
// اضبط مظهره ومحتوياته، ثم أضفه كعنصر فرعي إلى الفقرة.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## انظر أيضًا

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
