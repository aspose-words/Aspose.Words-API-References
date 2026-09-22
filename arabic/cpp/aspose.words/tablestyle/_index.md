---
title: "فئة Aspose::Words::TableStyle"
linktitle: "TableStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::TableStyle. تمثل نمط جدول. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 67000
url: /ar/cpp/aspose.words/tablestyle/
---
## TableStyle class


يمثل نمط جدول. لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | يقارن بالنمط المحدد. يتم مقارنة معرفات الأنماط للأنماط المدمجة فقط. لا تُضمّن القيم الافتراضية للأنماط في المقارنة. يتم مقارنة النمط الأساسي، والنمط المرتبط، ونمط الفقرة التالية بشكل متكرر. |
| [get_Aliases](../style/get_aliases/)() | يحصل على جميع الأسماء المستعارة لهذا النمط. إذا لم يكن للنمط أي أسماء مستعارة فسيتم إرجاع مصفوفة فارغة من السلاسل. |
| [get_Alignment](./get_alignment/)() | يحدد المحاذاة لنمط الجدول. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | يحصل أو يضبط علامة تشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة. |
| [get_BaseStyleName](../style/get_basestylename/)() | يحصل/يضبط اسم النمط الذي يُبنى عليه هذا النمط. |
| [get_Borders](./get_borders/)() | يحصل على مجموعة حدود الخلايا الافتراضية للنمط. |
| [get_BottomPadding](./get_bottompadding/)() | يحصل أو يحدد مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول. |
| [get_BuiltIn](../style/get_builtin/)() | صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word. |
| [get_CellSpacing](./get_cellspacing/)() | يحصل أو يضبط مقدار المسافة (بالنقاط) بين الخلايا. |
| [get_ColumnStripe](./get_columnstripe/)() | يحصل أو يضبط عدد الأعمدة التي تُضمّن في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | مجموعة من الأنماط الشرطية التي قد تُعرّف لهذا نمط الجدول. |
| [get_Document](../style/get_document/)() | يحصل على المستند المالِك. |
| [get_Font](../style/get_font/)() | يحصل على تنسيق الأحرف للنمط. |
| [get_IsHeading](../style/get_isheading/)() | صحيح عندما يكون النمط أحد أنماط العناوين المدمجة. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | يحدد ما إذا كان هذا النمط يُظهر في معرض [Style](../style/) السريع داخل واجهة مستخدم MS Word. |
| [get_LeftIndent](./get_leftindent/)() | يحصل أو يضبط القيمة التي تمثل المسافة البادئة اليسرى للجدول. |
| [get_LeftPadding](./get_leftpadding/)() | يحصل أو يحدد مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | يحصل/يضبط اسم الـ[Style](../style/) المرتبط بهذا. يُعيد سلسلة فارغة إذا لم يكن هناك أنماط مرتبطة. |
| [get_List](../style/get_list/)() | يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [get_ListFormat](../style/get_listformat/)() | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [get_Locked](../style/get_locked/)() const | يحدد ما إذا كان هذا النمط مقفلًا. |
| [get_Name](../style/get_name/)() const | يحصل أو يضبط اسم النمط. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | يحصل/يضبط اسم النمط الذي يُطبق تلقائيًا على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | يحصل على تنسيق الفقرة للنمط. |
| [get_Priority](../style/get_priority/)() const | يحصل/يضبط القيمة الصحيحة التي تمثل الأولوية لفرز الأنماط في لوحة مهام الأنماط. |
| [get_RightPadding](./get_rightpadding/)() | يحصل أو يحدد مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول. |
| [get_RowStripe](./get_rowstripe/)() | يحصل أو يضبط عدد الصفوف التي تُضمّن في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية. |
| [get_SemiHidden](../style/get_semihidden/)() const | يحصل/يضبط ما إذا كان النمط يختفي من معرض الأنماط ومن لوحة مهام الأنماط. |
| [get_Shading](./get_shading/)() | يحصل على كائن الـ[Shading](../shading/) الذي يشير إلى تنسيق التظليل لخلايا الجدول. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | يحصل على معرف النمط المستقل عن اللغة لنمط مدمج. |
| [get_Styles](../style/get_styles/)() const | يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [get_TopPadding](./get_toppadding/)() | يحصل أو يحدد مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول. |
| [get_Type](../style/get_type/)() const | يحصل على نوع النمط (فقرة أو حرف). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه مرة أخرى في معرض الأنماط ومن لوحة مهام الأنماط. يكون صحيحًا عندما يجب إظهار النمط المستخدم في معرض الأنماط. |
| [get_VerticalAlignment](./get_verticalalignment/)() | يحدد المحاذاة العمودية للخلايا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | يزيل النمط المحدد من المستند. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | مُعيّن لـ[Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | مُعيّن لـ[Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | مُعيّن لـ[Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | مُعيّن لـ[Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | مُعيّن لـ[Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | مُعيّن لـ[Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | مُعيّن لـ[Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | مُعيّن لـ[Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | مُعيّن لـ[Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | مُعيّن لـ[Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | محدد لـ [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | محدد لـ [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | محدد لـ [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | محدد لـ [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | محدد لـ [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | محدد لـ [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | محدد لـ [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | محدد لـ [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | محدد لـ [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// قد يؤدي ضبط خصائص النمط للجدول إلى تأثير على خصائص الجدول نفسه.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## انظر أيضًا

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
