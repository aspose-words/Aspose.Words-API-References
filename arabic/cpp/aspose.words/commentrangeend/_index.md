---
title: "Aspose::Words::CommentRangeEnd class"
linktitle: "CommentRangeEnd"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::CommentRangeEnd class. يشير إلى نهاية منطقة نصية لها تعليق مرتبط بها. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/commentrangeend/
---
## CommentRangeEnd class


يشير إلى نهاية منطقة نصية مرتبطة بتعليق. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentRangeEnd : public Aspose::Words::Node,
                        public Aspose::Words::IDisplaceableByCustomXml,
                        public Aspose::Words::INodeWithAnnotationId
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [CommentRangeEnd](./commentrangeend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Id](./get_id/)() const | يحدد معرف التعليق الذي ترتبط به هذه المنطقة. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يعيد [CommentRangeEnd](../nodetype/). |
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
| [set_Id](./set_id/)(int32_t) | يحدد معرف التعليق الذي ترتبط به هذه المنطقة. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


لإنشاء تعليق مرتبط بمنطقة نصية، تحتاج إلى إنشاء [Comment](../comment/) ثم إنشاء [CommentRangeStart](../commentrangestart/) و[CommentRangeEnd](./) وتعيين معرفاتهم إلى نفس قيمة [Id](../comment/get_id/).

[CommentRangeEnd](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

## انظر أيضًا

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
