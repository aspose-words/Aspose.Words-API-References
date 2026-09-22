---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument فئة"
linktitle: "GlossaryDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument فئة. يمثل العنصر الجذر لمستند مسرد داخل مستند Word. مستند المسرد هو مخزن لـ AutoText و AutoCorrect و Building Blocks. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class


يمثل العنصر الجذر لمستند مسرد داخل مستند Word. مستند المسرد هو مساحة تخزين لـ AutoText وإدخالات AutoCorrect و Building Blocks. لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class GlossaryDocument : public Aspose::Words::DocumentBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية مستند Glossary. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية مستند Glossary. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/)() const | يحصل أو يضبط شكل الخلفية للمستند. يمكن أن يكون **null**. |
| [get_BuildingBlocks](./get_buildingblocks/)() | يرجع مجموعة ذات نوع تمثل جميع كتل البناء في مستند المسرد. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_Document](../../aspose.words/documentbase/get_document/)() const override | يحصل على هذا الكائن. |
| [get_FirstBuildingBlock](./get_firstbuildingblock/)() | يحصل على أول كتلة بناء في مستند المسرد. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FontInfos](../../aspose.words/documentbase/get_fontinfos/)() const | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند. |
| [get_FootnoteSeparators](../../aspose.words/documentbase/get_footnoteseparators/)() const | يوفر الوصول إلى فواصل الحواشي السفلية/الختامية المعرفة في المستند. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_LastBuildingBlock](./get_lastbuildingblock/)() | يحصل على آخر كتلة بناء في مستند المسرد. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_Lists](../../aspose.words/documentbase/get_lists/)() const | يوفر الوصول إلى تنسيق القوائم المستخدم في المستند. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeChangingCallback](../../aspose.words/documentbase/get_nodechangingcallback/)() | يُستدعى عندما يتم إدراج عقدة أو إزالتها في المستند. |
| [get_NodeType](./get_nodetype/)() const override | يرجع القيمة [GlossaryDocument](../../aspose.words/nodetype/). |
| [get_PageColor](../../aspose.words/documentbase/get_pagecolor/)() | يحصل أو يعيّن لون الصفحة للمستند. هذه الخاصية هي نسخة مبسطة من [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_ResourceLoadingCallback](../../aspose.words/documentbase/get_resourceloadingcallback/)() const | يسمح بالتحكم في طريقة تحميل الموارد الخارجية. |
| [get_Styles](../../aspose.words/documentbase/get_styles/)() const | يرجع مجموعة من الأنماط المعرفة في المستند. |
| [get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/)() const | يُستدعى أثناء إجراءات معالجة المستند المختلفة عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetBuildingBlock](./getbuildingblock/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery, const System::String\&, const System::String\&) | يبحث عن كتلة بناء باستخدام المعرض والفئة والاسم المحددين. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يستورد عقدة من مستند آخر إلى المستند الحالي. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من العنصر الأب. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](../../aspose.words.markup/smarttag/) للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../../aspose.words/node/) يطابق تعبير XPath. |
| [set_BackgroundShape](../../aspose.words/documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | دالة تعيين لـ [Aspose::Words::DocumentBase::get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../../aspose.words/documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | يُستدعى عندما يتم إدراج عقدة أو إزالتها في المستند. |
| [set_PageColor](../../aspose.words/documentbase/set_pagecolor/)(System::Drawing::Color) | دالة تعيين لـ [Aspose::Words::DocumentBase::get_PageColor](../../aspose.words/documentbase/get_pagecolor/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](../../aspose.words/documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في طريقة تحميل الموارد الخارجية. |
| [set_WarningCallback](../../aspose.words/documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | دالة تعيين لـ [Aspose::Words::DocumentBase::get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


بعض المستندات، عادةً القوالب، يمكن أن تحتوي على AutoText و AutoCorrect و/أو Building Blocks (المعروفة أيضًا باسم *إدخالات مستند المسرد*، *أجزاء المستند* أو *كتل البناء*).

للوصول إلى كتل البناء، تحتاج إلى تحميل مستند إلى كائن [Document](../../aspose.words/document/). ستتوفر كتل البناء عبر خاصية [GlossaryDocument](../../aspose.words/document/get_glossarydocument/).

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects. Each [BuildingBlock](../buildingblock/) represents one document part.

يتطابق مع عناصر **glossaryDocument** و **docParts** في OOXML.

## انظر أيضًا

* Class [DocumentBase](../../aspose.words/documentbase/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
