---
title: "فئة Aspose::Words::Tables::Table"
linktitle: "Table"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Tables::Table. تمثل جدولًا في مستند Word. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.tables/table/
---
## Table class


يمثل جدولًا في مستند Word. لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class Table : public Aspose::Words::CompositeNode
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية الجدول. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية الجدول. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | يعيد تحجيم الجدول والخلايا وفقًا لسلوك الملاءمة التلقائي المحدد. |
| [ClearBorders](./clearborders/)() | يزيل جميع حدود الجدول والخلية في هذا الجدول. |
| [ClearShading](./clearshading/)() | يزيل جميع التظليل في الجدول. |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | يحوّل الخلايا المدمجة أفقيًا حسب العرض إلى خلايا مدمجة بواسطة [HorizontalMerge](../cellformat/get_horizontalmerge/). |
| [EnsureMinimum](./ensureminimum/)() | إذا لم يكن للجدول أي صفوف، ينشئ ويضيف صفًا واحدًا [Row](../row/). |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | يحصل أو يضبط موضع الجدول العائم الأفقي المطلق المحدد بخصائص الجدول، بالنقاط. القيمة الافتراضية هي 0. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | يحصل أو يضبط موضع الجدول العائم العمودي المطلق المحدد بخصائص الجدول، بالنقاط. القيمة الافتراضية هي 0. |
| [get_Alignment](./get_alignment/)() | يحدد كيفية محاذاة جدول مضمن في المستند. |
| [get_AllowAutoFit](./get_allowautofit/)() | يسمح لـ Microsoft Word و Aspose.Words بإعادة تحجيم الخلايا في جدول تلقائيًا لتناسب محتواها. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | يحصل أو يضبط خيار \"Allow spacing between cells\". |
| [get_AllowOverlap](./get_allowoverlap/)() | يحصل ما إذا كان الجدول العائم سيسمح لكائنات عائمة أخرى في المستند بتغطية نطاقه عند العرض. القيمة الافتراضية هي **true**. |
| [get_Bidi](./get_bidi/)() | يحصل أو يضبط ما إذا كان هذا جدولًا من اليمين إلى اليسار. |
| [get_BottomPadding](./get_bottompadding/)() | يحصل أو يضبط مقدار المسافة (بالنقاط) لإضافتها أسفل محتوى الخلايا. |
| [get_CellSpacing](./get_cellspacing/)() | يحصل أو يضبط مقدار المسافة (بالنقاط) بين الخلايا. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_Description](./get_description/)() | يحصل أو يضبط وصف هذا الجدول. يوفر تمثيلًا نصيًا بديلاً للمعلومات الموجودة في الجدول. |
| [get_DistanceBottom](./get_distancebottom/)() | يحصل أو يضبط المسافة بين أسفل الجدول والنص المحيط، بالنقاط. |
| [get_DistanceLeft](./get_distanceleft/)() | يحصل أو يضبط المسافة بين يسار الجدول والنص المحيط، بالنقاط. |
| [get_DistanceRight](./get_distanceright/)() | يحصل أو يضبط المسافة بين يمين الجدول والنص المحيط، بالنقاط. |
| [get_DistanceTop](./get_distancetop/)() | يحصل أو يضبط المسافة بين أعلى الجدول والنص المحيط، بالنقاط. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FirstRow](./get_firstrow/)() | يرجع أول عقدة [Row](../row/) في الجدول. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | يحصل على الكائن الأساسي الذي يجب حساب الموضع الأفقي للجدول العائم بناءً عليه. القيمة الافتراضية هي [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_LastRow](./get_lastrow/)() | يرجع آخر عقدة [Row](../row/) في الجدول. |
| [get_LeftIndent](./get_leftindent/)() | الحصول أو تعيين القيمة التي تمثل المسافة البادئة اليسرى للجدول. |
| [get_LeftPadding](./get_leftpadding/)() | الحصول أو تعيين مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات الخلايا. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يعيد [Table](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreferredWidth](./get_preferredwidth/)() | الحصول أو تعيين العرض المفضل للجدول. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | الحصول أو تعيين محاذاة الجدول العائم الأفقية النسبية. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | الحصول أو تعيين محاذاة الجدول العائم العمودية النسبية. |
| [get_RightPadding](./get_rightpadding/)() | الحصول أو تعيين مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات الخلايا. |
| [get_Rows](./get_rows/)() | يوفر وصولًا مكتوبًا للصفوف في الجدول. |
| [get_Style](./get_style/)() | الحصول أو تعيين نمط الجدول المطبق على هذا الجدول. |
| [get_StyleIdentifier](./get_styleidentifier/)() | الحصول أو تعيين معرف النمط المستقل عن الإعدادات الإقليمية لنمط الجدول المطبق على هذا الجدول. |
| [get_StyleName](./get_stylename/)() | الحصول أو تعيين اسم نمط الجدول المطبق على هذا الجدول. |
| [get_StyleOptions](./get_styleoptions/)() | الحصول أو تعيين أعلام البت التي تحدد كيفية تطبيق نمط الجدول على هذا الجدول. |
| [get_TextWrapping](./get_textwrapping/)() | الحصول أو تعيين [TextWrapping](./get_textwrapping/) للجدول. |
| [get_Title](./get_title/)() | الحصول أو تعيين عنوان هذا الجدول. يوفر تمثيلًا نصيًا بديلاً للمعلومات المحتواة في الجدول. |
| [get_TopPadding](./get_toppadding/)() | الحصول أو تعيين مقدار المسافة (بالنقاط) لإضافتها فوق محتويات الخلايا. |
| [get_VerticalAnchor](./get_verticalanchor/)() | الحصول على الكائن الأساسي الذي يجب حساب موضعه العمودي للجدول العائم بناءً عليه. القيمة الافتراضية هي [Margin](../../aspose.words.drawing/relativeverticalposition/). |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](../../aspose.words.markup/smarttag/) للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../../aspose.words/node/) يطابق تعبير XPath. |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/). |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | مُعيّن لـ [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/). |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | مُعيّن لـ [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/). |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | مُعيّن لـ [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/). |
| [set_Bidi](./set_bidi/)(bool) | مُعيّن لـ [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/). |
| [set_BottomPadding](./set_bottompadding/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Tables::Table::get_Description](./get_description/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/). |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | مُعيّن لـ [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/). |
| [set_LeftIndent](./set_leftindent/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | مُعيّن لـ [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | مُعيّن لـ [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/). |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | مُعيّن لـ [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/). |
| [set_RightPadding](./set_rightpadding/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | مُعيّن لـ [Aspose::Words::Tables::Table::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | مُعيّن لـ [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/). |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | مُعيّن لـ [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/). |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | مُعيّن لـ [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/). |
| [set_Title](./set_title/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Tables::Table::get_Title](./get_title/). |
| [set_TopPadding](./set_toppadding/)(double) | مُعيّن لـ [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | مُعيّن لـ [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/). |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | يضبط حد الجدول المحدد إلى نمط الخط والعرض واللون المحددين. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | يضبط جميع حدود الجدول إلى نمط الخط والعرض واللون المحددين. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | يضبط التظليل إلى القيم المحددة على كامل الجدول. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | ينشئ مثيلاً جديداً من الفئة [Table](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

يجب أن يحتوي جدول صالح بسيط على صف واحد على الأقل [Row](../row/).

## أمثلة



يظهر كيفية إنشاء جدول منسق 2×2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// أثناء بناء الجدول، سيطبق مُنشئ المستند قيم خصائص RowFormat/CellFormat الحالية.
// على الصف/الخلية الحالية التي يقع فيها المؤشر وأي صفوف/خلايا جديدة يتم إنشاؤها.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// الصفوف والخلايا التي أضيفت مسبقًا لا تتأثر بأية تغييرات لاحقة على تنسيق المُنشئ.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


يعرض كيفية إنشاء جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// الجداول تحتوي على صفوف، والتي تحتوي على خلايا، والتي قد تحتوي على فقرات
// مع عناصر نمطية مثل السلاسل، الأشكال، وحتى جداول أخرى.
// استدعاء طريقة "EnsureMinimum" على جدول سيضمن أن
// الجدول يحتوي على صف واحد على الأقل، وخلية، وفقرة.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// أضف نصًا إلى الخلية الأولى في الصف الأول من الجدول.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


يظهر كيفية التكرار عبر جميع الجداول في المستند وطباعة محتويات كل خلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // يمكننا استخدام طريقة "ToArray" على مجموعة الصفوف لاستنساخها إلى مصفوفة.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // يمكننا استخدام طريقة "ToArray" على مجموعة الخلايا لاستنساخها إلى مصفوفة.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## انظر أيضًا

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
