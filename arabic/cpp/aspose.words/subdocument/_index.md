---
title: "فئة Aspose::Words::SubDocument"
linktitle: "SubDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::SubDocument. تمثل SubDocument - وهو إشارة إلى مستند مخزن خارجيًا. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 66000
url: /ar/cpp/aspose.words/subdocument/
---
## SubDocument class


يمثل **SubDocument** - وهو إشارة إلى مستند مخزن خارجيًا. لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class SubDocument : public Aspose::Words::Node
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يعيد [SubDocument](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../node/remove/)() | يزيل نفسه من العنصر الأب. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


في هذا الإصدار من Aspose.Words، لا توفر عقد [SubDocument](./) طرقًا عامة وخصائص لإنشاء أو تعديل مستند فرعي. في هذا الإصدار لا يمكنك إنشاء عقد [SubDocument](./) أو تعديل الموجودة باستثناء حذفها.

[SubDocument](./) can only be a child of [Paragraph](../paragraph/).

## أمثلة



يظهر كيفية الوصول إلى المستند الفرعي للوثيقة الرئيسية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// تعمل هذه العقدة كمرجع إلى مستند خارجي، ولا يمكن الوصول إلى محتوياتها.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## انظر أيضًا

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
