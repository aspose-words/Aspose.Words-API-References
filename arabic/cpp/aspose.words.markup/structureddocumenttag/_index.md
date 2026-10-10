---
title: "فئة Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Markup::StructuredDocumentTag. تمثل علامة مستند مُنظمة (SDT أو عنصر تحكم محتوى) في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


يمثل علامة مستند مُنظم (SDT أو عنصر تحكم محتوى) في مستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية الـ [StructuredDocumentTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية الـ [StructuredDocumentTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | يمسح محتويات هذه العلامة المُنظمة ويعرض عنصرًا نائبًا إذا تم تعريفه. |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_Appearance](./get_appearance/)() override | يحصل/يضبط مظهر العلامة المُنظمة. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | يحدد فئة كتلة البناء لهذه العقدة **SDT**. لا يمكن أن تكون **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | يحدد نوع كتلة البناء لهذه **SDT**. لا يمكن أن تكون **null**. |
| [get_CalendarType](./get_calendartype/)() | يحدد نوع التقويم لهذه **SDT**. القيمة الافتراضية هي [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | يحصل/يضبط الحالة الحالية لمربع الاختيار **SDT**. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_Color](./get_color/)() override | يحصل أو يضبط لون علامة المستند المهيكلة. |
| [get_ContentsFont](./get_contentsfont/)() | تنسيق [Font](../../aspose.words/font/) الذي سيُطبق على النص المدخل في **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | سلسلة تمثل الصيغة التي تُعرض بها التواريخ. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | يسمح بتعيين/الحصول على تنسيق اللغة للتاريخ المعروض في هذه **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | يحصل/يضبط الصيغة التي يُخزن بها التاريخ لعلامة تاريخ **SDT** عندما تكون **SDT** مرتبطة بعقدة XML في مخزن بيانات المستند. القيمة الافتراضية هي [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | تنسيق [Font](../../aspose.words/font/) الذي سيُطبق على الحرف الأخير من النص المدخل في **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FullDate](./get_fulldate/)() | يحدد التاريخ والوقت الكاملين اللذين تم إدخالهما آخرًا في هذه **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_Id](./get_id/)() override | يحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمرًا لهذا **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | يحدد ما إذا كان محتوى هذه **SDT** سيُفسَّر على أنه يحتوي على نص نائب (بدلاً من محتوى نص عادي داخل الـ SDT). إذا تم تعيينه إلى **true**، سيُستأنف هذا الحالة (عرض نص نائب) عند فتح هذا المستند. |
| [get_IsTemporary](./get_istemporary/)() const | يحدد ما إذا كانت هذه **SDT** ستُزال من مستند WordProcessingML عندما يتم تعديل محتوياتها. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_Level](./get_level/)() const override | يحصل على المستوى الذي يحدث فيه هذا **SDT** في شجرة المستند. |
| [get_ListItems](./get_listitems/)() | يحصل على [SdtListItemCollection](../sdtlistitemcollection/) المرتبط بهذه **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | عند تعيينه إلى **true**، ستمنع هذه الخاصية المستخدم من حذف هذه **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | عند تعيينه إلى **true**، ستمنع هذه الخاصية المستخدم من تعديل محتويات هذه **SDT**. |
| [get_Multiline](./get_multiline/)() | يحدد ما إذا كان هذا **SDT** يسمح بعدة أسطر من النص. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_Placeholder](./get_placeholder/)() override | يحصل على [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص العنصر النائب الذي يجب عرضه عندما تكون محتويات تشغيل هذا SDT فارغة، أو يكون عنصر XML المرتبط فارغًا كما هو محدد عبر عنصر [XmlMapping](./get_xmlmapping/) أو يكون عنصر [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | يحصل أو يضبط اسم [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص نائب. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_SdtType](./get_sdttype/)() override | يحصل على نوع هذه **Structured document tag**. |
| [get_Style](./get_style/)() | يحصل أو يعيّن [Style](../../aspose.words/style/) لعلامة المستند المهيكلة. |
| [get_StyleName](./get_stylename/)() | يحصل أو يعيّن اسم النمط المطبّق على علامة المستند المهيكلة. |
| [get_Tag](./get_tag/)() const override | يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن تكون **null**. |
| [get_Title](./get_title/)() const override | يحدد الاسم الودي المرتبط بهذا **SDT**. لا يمكن أن يكون **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | يحصل على سلسلة تمثل XML الموجود داخل العقدة بصيغة [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [FlatOpc](../../aspose.words/saveformat/). على عكس خاصية [WordOpenXML](./get_wordopenxml/)، تُنشئ هذه الطريقة مستندًا مبسطًا يستثني أي أجزاء غير متعلقة بالمحتوى. |
| [get_XmlMapping](./get_xmlmapping/)() override | يحصل على كائن يمثل تخطيط هذه علامة المستند المهيكلة إلى بيانات XML في جزء XML مخصص للمستند الحالي. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
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
| [RemoveSelfOnly](./removeselfonly/)() override | يزيل عقدة الـ SDT هذه فقط، لكنه يحتفظ بمحتواها داخل شجرة المستند. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل جميع عقد [SmartTag](../smarttag/) التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../../aspose.words/node/) يطابق تعبير XPath. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | محدد لـ [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | معين لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | معين لـ [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | معين لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | معين لـ [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | يضبط الرمز المستخدم لتمثيل الحالة المحددة لمربع اختيار عنصر التحكم بالمحتوى. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | يضبط الرمز المستخدم لتمثيل الحالة غير المحددة لمربع اختيار عنصر التحكم بالمحتوى. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | ينشئ مثيلاً جديداً لفئة **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


تسمح علامات المستند المهيكلة (SDTs) بإدراج الدلالات المعرفة من قبل العميل بالإضافة إلى سلوكها ومظهرها داخل المستند.

في هذا الإصدار، توفر Aspose.Words عددًا من الطرق العامة والخصائص للتلاعب بسلوك ومحتوى [StructuredDocumentTag](./). يمكن تنفيذ ربط عقد SDT بحزم XML مخصصة داخل المستند باستخدام خاصية [XmlMapping](./get_xmlmapping/).

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## أمثلة



يوضح كيفية العمل مع الأنماط لعناصر التحكم بالمحتوى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند إلى StructuredDocumentTag.
// 1 -  تطبيق كائن نمط من مجموعة أنماط المستند:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  الإشارة إلى نمط في المستند بالاسم:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## انظر أيضًا

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
