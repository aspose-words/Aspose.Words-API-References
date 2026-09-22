---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart فئة"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart فئة. تمثل بداية علامة مستند منسقة ذات نطاق تقبل محتوى متعدد الأقسام. راجع أيضًا StructuredDocumentTagRangeEnd. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


تمثل بداية **ranged** لعلامة مستند منسقة ذات نطاق تقبل محتوى متعدد الأقسام. راجع أيضًا [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). لمعرفة المزيد، زر مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف العقدة المحددة إلى نهاية نطاق stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_Appearance](./get_appearance/)() override | يحصل أو يضبط مظهر علامة المستند المهيكلة. |
| [get_Color](./get_color/)() override | يحصل أو يضبط لون علامة المستند المهيكلة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Id](./get_id/)() override | يحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمر لهذا وسم مستند منسق. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | يحدد ما إذا كان محتوى هذا وسم المستند المنسق سيُفسَّر على أنه يحتوي على نص نائب (على عكس محتويات النص العادي داخل وسم المستند المنسق). إذا تم تعيينه إلى **true**، ستُستأنف هذه الحالة (عرض نص النائب) عند فتح هذا المستند. |
| [get_LastChild](./get_lastchild/)() | يحصل على العنصر الفرعي الأخير في نطاق stdContent. |
| [get_Level](./get_level/)() const override | يحصل على المستوى الذي يحدث فيه بدء نطاق وسم المستند المنسق في شجرة المستند. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | عند تعيينه إلى **true**، ستمنع هذه الخاصية المستخدم من حذف هذا وسم المستند المنسق. |
| [get_LockContents](./get_lockcontents/)() override | عند تعيينه إلى **true**، ستمنع هذه الخاصية المستخدم من تعديل محتويات هذا وسم المستند المنسق. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_Placeholder](./get_placeholder/)() override | يحصل على [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص نائب يجب عرضه عندما تكون محتويات تشغيل وسم المستند المنسق فارغة، أو يكون عنصر XML المرتبط فارغًا كما هو محدد عبر عنصر [XmlMapping](./get_xmlmapping/)، أو يكون عنصر [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | يحصل أو يضبط اسم [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص نائب. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_RangeEnd](./get_rangeend/)() | يحدد نهاية النطاق إذا كان [StructuredDocumentTag](../structureddocumenttag/) وسم مستند منسق ذو نطاق. وإلا يرجع **null**. |
| [get_SdtType](./get_sdttype/)() override | يحصل على نوع هذا وسم المستند المنسق. |
| [get_Tag](./get_tag/)() const override | يحدد وسمًا مرتبطًا بعقدة وسم المستند المنسق الحالي. لا يمكن أن يكون **null**. |
| [get_Title](./get_title/)() const override | يحدد الاسم الودي المرتبط بهذا وسم المستند المنسق. لا يمكن أن يكون **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | يحصل على سلسلة تمثل XML الموجود داخل العقدة بصيغة [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [FlatOpc](../../aspose.words/saveformat/). على عكس خاصية [WordOpenXML](./get_wordopenxml/)، تُنشئ هذه الطريقة مستندًا مبسطًا يستثني أي أجزاء غير متعلقة بالمحتوى. |
| [get_XmlMapping](./get_xmlmapping/)() override | يحصل على كائن يمثل ربط نطاق وسم المستند المنسق ببيانات XML في جزء XML مخصص للمستند الحالي. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | يرجع مجموعة حية من العقد الفرعية التي تطابق الأنواع المحددة. |
| [GetEnumerator](./getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من العنصر الأب. |
| [RemoveAllChildren](./removeallchildren/)() | يزيل جميع العقد بين عقدة بدء هذا النطاق وعقدة نهاية النطاق. |
| [RemoveSelfOnly](./removeselfonly/)() override | يزيل بدء هذا النطاق والعقد المناسبة لنهاية النطاق لوسم المستند المنسق، لكنه يحتفظ بمحتواه داخل شجرة المستند. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | مُعيّن لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | مُعيّن لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | مُعيّن لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | مُعيّن لـ [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | يُنشئ مثيلًا جديدًا للفئة **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية الحصول على خصائص العلامات المهيكلة للمستند متعددة الأقسام.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## انظر أيضًا

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
