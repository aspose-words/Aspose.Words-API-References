---
title: "Aspose::Words::PageSetup class"
linktitle: "PageSetup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup class. يمثل خصائص إعداد الصفحة لقسم. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 46000
url: /ar/cpp/aspose.words/pagesetup/
---
## PageSetup class


يمثل خصائص إعداد الصفحة لقسم. لمعرفة المزيد، زر مقالة الوثائق [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يعيد إعداد الصفحة إلى حجم الورق الافتراضي، الهوامش والاتجاه. |
| [get_Bidi](./get_bidi/)() | يحدد أن هذا القسم يحتوي على نص ثنائي الاتجاه (نصوص معقدة). |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | يحدد موضع حد الصفحة بالنسبة للنصوص والكائنات المتقاطعّة. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | يحدد الصفحات التي يُطبع عليها حد الصفحة. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | يحصل أو يعيّن قيمة تشير إلى ما إذا كان حد الصفحة المحدد يُقاس من حافة الصفحة أو من النص الذي يحيط به. |
| [get_Borders](./get_borders/)() | يحصل على مجموعة من حدود الصفحة. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | يحدد ما إذا كان حد الصفحة يشمل أو يستثني التذييل. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | يحدد ما إذا كان حد الصفحة يشمل أو يستثني الرأس. |
| [get_BottomMargin](./get_bottommargin/)() | يرجع أو يعيّن المسافة (بالنقاط) بين الحافة السفلية للصفحة والحد السفلي لنص الجسم. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | يحصل أو يعيّن حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة. |
| [get_CharactersPerLine](./get_charactersperline/)() | يحصل أو يعيّن عدد الأحرف في كل سطر في شبكة المستند. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | صحيح إذا تم استخدام رأس أو تذييل مختلف في الصفحة الأولى. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | يوفر خيارات تتحكم في ترقيم وتحديد موضع الحواشي السفلية في هذا القسم. |
| [get_FirstPageTray](./get_firstpagetray/)() | يحصل على صينية الورق (المستودع) المستخدمة للصفحة الأولى من القسم. القيمة خاصة بالتنفيذ (الطابعة). |
| [get_FooterDistance](./get_footerdistance/)() | يعيد أو يعيّن المسافة (بالنقاط) بين التذييل وأسفل الصفحة. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | يوفر خيارات تتحكم في ترقيم وتحديد موضع الحواشي السفلية في هذا القسم. |
| [get_Gutter](./get_gutter/)() | يحصل أو يعيّن مقدار المسافة الإضافية المضافة إلى الهامش لتثبيت المستند. |
| [get_HeaderDistance](./get_headerdistance/)() | يعيد أو يعيّن المسافة (بالنقاط) بين الرأس وأعلى الصفحة. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | يحصل أو يعيّن نمط مستوى العنوان المطبق على عناوين الفصول في المستند. |
| [get_LayoutMode](./get_layoutmode/)() | يحصل أو يعيّن وضع التخطيط لهذا القسم. |
| [get_LeftMargin](./get_leftmargin/)() | يعيد أو يعيّن المسافة (بالنقاط) بين الحافة اليسرى للصفحة والحد الأيسر للنص الأساسي. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | يعيد أو يعيّن الزيادة الرقمية لأرقام الأسطر. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | يحصل أو يعيّن المسافة بين الحافة اليمنى لأرقام الأسطر والحافة اليسرى للمستند. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | يحصل أو يعيّن طريقة تشغيل ترقيم الأسطر، أي ما إذا كان يبدأ من جديد في بداية صفحة أو قسم جديد أو يستمر بشكل مستمر. |
| [get_LinesPerPage](./get_linesperpage/)() | يحصل أو يعيّن عدد الأسطر في كل صفحة في شبكة المستند. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | يحصل أو يعيّن رقم السطر الابتدائي. |
| [get_Margins](./get_margins/)() | يعيد أو يعيّن إعدادات [Margins](../margins/) المسبقة للصفحة. |
| [get_MultiplePages](./get_multiplepages/)() const | بالنسبة للمستندات متعددة الصفحات، يحصل أو يعيّن كيفية طباعة أو عرض المستند بحيث يمكن تجميعه ككتيب. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | صحيح إذا كان المستند يحتوي على رؤوس وتذييلات مختلفة للصفحات ذات الأرقام الفردية والزوجية. |
| [get_Orientation](./get_orientation/)() | يعيد أو يعيّن اتجاه الصفحة. |
| [get_OtherPagesTray](./get_otherpagestray/)() | يحصل على صينية الورق (المستودع) المستخدمة لجميع الصفحات ما عدا الأولى في القسم. القيمة خاصة بالتنفيذ (الطابعة). |
| [get_PageHeight](./get_pageheight/)() | يعيد أو يعيّن ارتفاع الصفحة بالنقاط. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | يحصل أو يعيّن تنسيق رقم الصفحة. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | يحصل أو يعيّن رقم الصفحة الابتدائي للقسم. |
| [get_PageWidth](./get_pagewidth/)() | إرجاع أو تعيين عرض الصفحة بالنقاط. |
| [get_PaperSize](./get_papersize/)() | إرجاع أو تعيين حجم الورق. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | صحيح إذا كان ترقيم الصفحات يعيد البدء في بداية القسم. |
| [get_RightMargin](./get_rightmargin/)() | إرجاع أو تعيين المسافة (بالنقاط) بين الحافة اليمنى للصفحة والحد الأيمن للنص الأساسي. |
| [get_RtlGutter](./get_rtlgutter/)() | إحضار أو تعيين ما إذا كان Microsoft Word يستخدم الفواصل للقسم بناءً على لغة من اليمين إلى اليسار أو من اليسار إلى اليمين. |
| [get_SectionStart](./get_sectionstart/)() | إرجاع أو تعيين نوع فاصل القسم للكائن المحدد. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | إرجاع أو تعيين عدد الصفحات التي سيتم تضمينها في كل كتيب. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | صحيح إذا تم طباعة الحواشي السفلية في نهاية القسم التالي الذي لا يقمع الحواشي السفلية. تُطبع الحواشي السفلية المقموعة قبل الحواشي السفلية في ذلك القسم. |
| [get_TextColumns](./get_textcolumns/)() | إرجاع مجموعة تمثل مجموعة أعمدة النص. |
| [get_TextOrientation](./get_textorientation/)() | السماح بتحديد [TextOrientation](./get_textorientation/) للصفحة بأكملها. القيمة الافتراضية هي [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | إرجاع أو تعيين المسافة (بالنقاط) بين الحافة العلوية للصفحة والحد العلوي للنص الأساسي. |
| [get_VerticalAlignment](./get_verticalalignment/)() | إرجاع أو تعيين محاذاة النص العمودية على كل صفحة في مستند أو قسم. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | مُعيّن لـ [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | مُعيّن لـ [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | مُعيّن لـ [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | مُعيّن لـ [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | مُعيّن لـ [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | مُعيّن لـ [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | مُعيّن لـ [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | مُعيّن لـ [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | مُعيّن لـ [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | مُعيّن لـ [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | تعيين صينية الورق (الحاوية) المستخدمة للصفحة الأولى من القسم. القيمة خاصة بالتنفيذ (الطابعة). |
| [set_FooterDistance](./set_footerdistance/)(double) | مُعيّن لـ [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | مُعيّن لـ [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | المحدد لـ [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | المحدد لـ [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | المحدد لـ [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | المحدد لـ [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | المحدد لـ [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | المحدد لـ [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | المحدد لـ [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | المحدد لـ [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | المحدد لـ [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | المحدد لـ [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | المحدد لـ [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | المحدد لـ [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | المحدد لـ [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | يضبط صينية الورق (الصندوق) التي تُستخدم لجميع الصفحات ما عدا الصفحة الأولى في القسم. القيمة تعتمد على التنفيذ (الطابعة). |
| [set_PageHeight](./set_pageheight/)(double) | المحدد لـ [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | المحدد لـ [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | المحدد لـ [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | المحدد لـ [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | المحدد لـ [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | المحدد لـ [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | المحدد لـ [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | المحدد لـ [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | المحدد لـ [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | المحدد لـ [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | صحيح إذا تم طباعة الحواشي السفلية في نهاية القسم التالي الذي لا يقمع الحواشي السفلية. تُطبع الحواشي السفلية المقموعة قبل الحواشي السفلية في ذلك القسم. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | المحدد لـ [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | دالة تعيين لـ [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | دالة تعيين لـ [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## ملاحظات


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## أمثلة



يُظهر كيفية تطبيق وإرجاع إعدادات إعداد الصفحة إلى الأقسام في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عدّل خصائص إعداد الصفحة للقسم الحالي للمنشئ وأضف نصًا.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// إذا بدأنا قسمًا جديدًا باستخدام منشئ المستند،
// سوف يرث خصائص إعداد الصفحة الحالية للمنشئ.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// يمكننا إرجاع خصائص إعداد الصفحة الخاصة به إلى القيم الافتراضية باستخدام طريقة "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
