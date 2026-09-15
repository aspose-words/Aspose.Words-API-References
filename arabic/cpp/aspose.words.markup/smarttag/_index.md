---
title: "Aspose::Words::Markup::SmartTag class"
linktitle: "SmartTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::SmartTag class. تحدد هذه العنصر وجود علامة ذكية حول هيكل (هياكل) مضمنة واحدة أو أكثر (تشغيلات، صور، حقول، إلخ) داخل فقرة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.markup/smarttag/
---
## SmartTag class


هذا العنصر يحدد وجود علامة ذكية حول بنية داخلية واحدة أو أكثر (تشغيلات، صور، حقول، إلخ) داخل فقرة. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SmartTag : public Aspose::Words::CompositeNode,
                 public Aspose::Words::Markup::IMarkupNode
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية [SmartTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية [SmartTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Element](./get_element/)() const | يحدد اسم العلامة الذكية داخل المستند. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [SmartTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Properties](./get_properties/)() const | مجموعة من خصائص العلامة الذكية. |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_Uri](./get_uri/)() const | يحدد URI مساحة الاسم للعلامة الذكية. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](./) من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../../aspose.words/node/) يطابق تعبير XPath. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Element](./set_element/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Markup::SmartTag::get_Element](./get_element/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Uri](./set_uri/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Markup::SmartTag::get_Uri](./get_uri/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SmartTag](./smarttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | يُهيئ نسخة جديدة من الفئة [SmartTag](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


العلامات الذكية هي نوع من ترميز XML المخصص. توفر العلامات الذكية وسيلة لتضمين الدلالات التي يحددها العميل في المستند عبر القدرة على توفير مساحة اسم/اسم أساسية لتشغيل أو مجموعة من التشغيلات داخل المستند.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or another [SmartTag](./) node.

القائمة الكاملة لعقد الأطفال التي يمكن أن تظهر داخل علامة ذكية تتكون من [BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [CommentRangeStart](../../aspose.words/commentrangestart/), [CommentRangeEnd](../../aspose.words/commentrangeend/), [SmartTag](./).
## انظر أيضًا

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
