---
title: "Aspose::Words::Story class"
linktitle: "قصة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Story class. الفئة الأساسية للعناصر التي تحتوي على عقد على مستوى الكتلة الفقرة والجدول. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 63000
url: /ar/cpp/aspose.words/story/
---
## Story class


الفئة الأساسية للعناصر التي تحتوي على عقد على مستوى الكتلة [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). لمعرفة المزيد، زر مقالة الوثائق [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Story : public Aspose::Words::CompositeNode,
              public Aspose::Words::IStory
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | يقبل زائرًا. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXEnd لزائر المستند المحدد. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXStart لزائر المستند المحدد. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](./appendparagraph/)(const System::String\&) | طريقة مختصرة تنشئ كائنًا من نوع [Paragraph](../paragraph/) مع نص اختياري وتضيفه إلى نهاية هذا الكائن. |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [DeleteShapes](./deleteshapes/)() | يحذف جميع الأشكال من نص هذه القصة. |
| [get_Count](../compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FirstParagraph](./get_firstparagraph/)() override | يحصل على الفقرة الأولى في القصة. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_LastChild](../compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_LastParagraph](./get_lastparagraph/)() override | يحصل على الفقرة الأخيرة في القصة. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| virtual [get_NodeType](../node/get_nodetype/)() const | يحصل على نوع هذه العقدة. |
| [get_Paragraphs](./get_paragraphs/)() override | يحصل على مجموعة من الفقرات التي هي أطفال مباشرون للقصة. |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_StoryType](./get_storytype/)() override | يحصل على نوع هذه القصة. |
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


يُقال إن نص مستند Word يتكون من عدة قصص. يُخزن النص الرئيسي في قصة النص الرئيسية الممثلة بـ[Body](../body/)، كل رأس وتذييل يُخزن في قصة منفصلة ممثلة بـ[HeaderFooter](../headerfooter/).

## أمثلة



يُظهر كيفية إزالة جميع الأشكال من عقدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمن،
// الذي له فقرة أصل، وهي عقدة فرعية لجسم القسم الأول.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## انظر أيضًا

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
