---
title: "فئة Aspose::Words::DocumentBase"
linktitle: "DocumentBase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::DocumentBase. توفر الفئة الأساسية المجردة لمستند رئيسي ومستند مسرد لمستند Word. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words/documentbase/
---
## DocumentBase class


يوفر الفئة الأساسية المجردة للمستند الرئيسي ومستند الفهرس في مستند Word. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | يقبل زائرًا. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXEnd لزائر المستند المحدد. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | عند تنفيذها في فئة مشتقة، تستدعي طريقة VisitXXXStart لزائر المستند المحدد. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_BackgroundShape](./get_backgroundshape/)() const | يحصل أو يضبط شكل الخلفية للمستند. يمكن أن يكون **null**. |
| [get_Count](../compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_Document](./get_document/)() const override | يحصل على هذا الكائن. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FontInfos](./get_fontinfos/)() const | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند. |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | يوفر الوصول إلى فواصل الحواشي السفلية/الختامية المعرفة في المستند. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_LastChild](../compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_Lists](./get_lists/)() const | يوفر الوصول إلى تنسيق القوائم المستخدم في المستند. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | يُستدعى عندما يتم إدراج عقدة أو إزالتها في المستند. |
| virtual [get_NodeType](../node/get_nodetype/)() const | يحصل على نوع هذه العقدة. |
| [get_PageColor](./get_pagecolor/)() | يحصل أو يعيّن لون الصفحة للمستند. هذه الخاصية نسخة أبسط من [BackgroundShape](./get_backgroundshape/). |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | يسمح بالتحكم في طريقة تحميل الموارد الخارجية. |
| [get_Styles](./get_styles/)() const | يرجع مجموعة من الأنماط المعرفة في المستند. |
| [get_WarningCallback](./get_warningcallback/)() const | يُستدعى أثناء إجراءات معالجة المستند المختلفة عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetText](../compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يستورد عقدة من مستند آخر إلى المستند الحالي. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق. |
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
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | مُعيّن لـ [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | يُستدعى عندما يتم إدراج عقدة أو إزالتها في المستند. |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في طريقة تحميل الموارد الخارجية. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | مُعيّن لـ [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


تمثل Aspose.Words مستند Word كشجرة من العقد. [DocumentBase](./) هي عقدة جذرية للشجرة تحتوي على جميع العقد الأخرى للمستند.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## أمثلة



يوضح كيفية تهيئة الفئات الفرعية لـ [DocumentBase](./).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## انظر أيضًا

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
