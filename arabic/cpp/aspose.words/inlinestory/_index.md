---
title: "Aspose::Words::InlineStory فئة"
linktitle: "InlineStory"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::InlineStory فئة. الفئة الأساسية للعقد ذات المستوى المضمن الذي يمكنه احتواء فقرات وجداول. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 37000
url: /ar/cpp/aspose.words/inlinestory/
---
## InlineStory class


الفئة الأساسية لعقد المستوى الداخلي التي يمكن أن تحتوي على فقرات وجداول. لمعرفة المزيد، زر مقالة الوثائق [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/)

```cpp
class InlineStory : public Aspose::Words::CompositeNode,
                    public Aspose::Words::IInline,
                    public Aspose::Words::IStory
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | يقبل زائرًا. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXEnd لزائر المستند المحدد. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXStart لزائر المستند المحدد. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [EnsureMinimum](./ensureminimum/)() | إذا لم يكن العنصر الفرعي الأخير فقرة، ينشئ ويضيف فقرة فارغة واحدة. |
| [get_Count](../compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FirstParagraph](./get_firstparagraph/)() override | يحصل على الفقرة الأولى في القصة. |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لحرف المرجع لهذا الكائن. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_LastChild](../compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_LastParagraph](./get_lastparagraph/)() override | يحصل على الفقرة الأخيرة في القصة. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| virtual [get_NodeType](../node/get_nodetype/)() const | يحصل على نوع هذه العقدة. |
| [get_Paragraphs](./get_paragraphs/)() override | يحصل على مجموعة من الفقرات التي هي أطفال مباشرون للقصة. |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](./get_parentparagraph/)() | يسترجع العنصر الأب [Paragraph](../paragraph/) لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| virtual [get_StoryType](./get_storytype/)() | يعيد نوع القصة. |
| [get_Tables](./get_tables/)() override | يحصل على مجموعة من الجداول التي هي أطفال مباشرون للقصة. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetText](../compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
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


[InlineStory](./) is a container for block-level nodes [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/).

الفئات التي تُشتق من [InlineStory](./) هي عقد ذات مستوى مضمن يمكنها احتواء نصها الخاص (فقرات وجداول). على سبيل المثال، عقدة [Comment](../comment/) تحتوي على نص التعليق وعقدة [Footnote](../../aspose.words.notes/footnote/) تحتوي على نص الحاشية.

## أمثلة



يوضح كيفية إدراج وتخصيص الحواشي السفلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستضع هذه الحاشية السفلية إشارة صغيرة مرتفعة
// بعد النص الذي تشير إليه وتُنشئ إدخالًا أسفل النص الرئيسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على علامة الإشارة الخاصة بالحاشية السفلية والنص المرجعي،
// والتي سنمررها إلى طريقة "InsertFootnote" الخاصة بـ document builder.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// إذا تم ضبط هذه الخاصية إلى "true"، فإن علامة الإشارة الخاصة بحاشيتنا السفلية
// ستكون مؤشرها بين جميع حواشي القسم.
// هذه هي الحاشية السفلية الأولى، لذا ستكون علامة الإشارة "1".
ASSERT_TRUE(footnote->get_IsAuto());

// يمكننا نقل document builder داخل الحاشية السفلية لتعديل نص الإشارة الخاص بها.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// يمكننا ضبط علامة إشارة مخصصة ستستخدمها الحاشية السفلية بدلًا من رقم مؤشرها.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// إشارة مرجعية مع العلم "IsAuto" مضبوط على true ستظهر مؤشرها الحقيقي
// حتى وإن كانت الإشارات المرجعية السابقة تعرض علامات إشارة مخصصة، فإن علامة الإشارة لهذه الإشارة المرجعية ستكون "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```


يعرض كيفية إضافة تعليق إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// في Microsoft Word، يمكننا النقر بزر الماوس الأيمن على هذا التعليق في جسم المستند لتعديله، أو الرد عليه.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## انظر أيضًا

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
