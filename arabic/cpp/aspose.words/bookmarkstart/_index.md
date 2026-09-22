---
title: "Aspose::Words::BookmarkStart class"
linktitle: "BookmarkStart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BookmarkStart class. يمثل بداية إشارة مرجعية في مستند Word. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/bookmarkstart/
---
## BookmarkStart class


يمثل بداية علامة مرجعية في مستند Word. لمعرفة المزيد، زر مقالة الوثائق [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkStart : public Aspose::Words::Node,
                      public Aspose::Words::IBookmarkNode,
                      public Aspose::Words::IDisplaceableByCustomXml
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [BookmarkStart](./bookmarkstart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | ينشئ نسخة جديدة من الفئة [BookmarkStart](./). |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_Bookmark](./get_bookmark/)() | يحصل على كائن الواجهة الذي يضمّ بداية ونهاية هذه الإشارة المرجعية. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_Name](./get_name/)() override | يحصل على اسم الإشارة المرجعية. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [BookmarkStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | يرجع سلسلة فارغة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../node/remove/)() | يزيل نفسه من العنصر الأب. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Name](./set_name/)(System::String) override | يضبط اسم الإشارة المرجعية. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


تتكون إشارة مرجعية كاملة في مستند Word من [BookmarkStart](./) و[BookmarkEnd](../bookmarkend/) متطابقين يحملان نفس اسم الإشارة المرجعية.

[BookmarkStart](./) and [BookmarkEnd](../bookmarkend/) are just markers inside a document that specify where the bookmark starts and ends.

استخدم الفئة [Bookmark](./get_bookmark/) كـ "واجهة" للعمل مع إشارة مرجعية ككائن واحد.
## انظر أيضًا

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
