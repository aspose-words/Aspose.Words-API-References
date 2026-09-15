---
title: "Aspose::Words::ParagraphFormat فئة"
linktitle: "ParagraphFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat فئة. تمثل جميع تنسيقات الفقرة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 49000
url: /ar/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


يمثل جميع تنسيقات الفقرة. لمعرفة المزيد، زر مقالة الوثائق [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يعيد الضبط إلى تنسيق الفقرة الافتراضي. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | يحصل أو يعيّن علامة تشير إلى ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق النص اللاتيني ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | يحصل أو يعيّن علامة تشير إلى ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق الأرقام ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |
| [get_Alignment](./get_alignment/)() | يحصل أو يضبط محاذاة النص للفقرة. |
| [get_BaselineAlignment](./get_baselinealignment/)() | يحصل أو يضبط الموضع العمودي للخطوط على السطر. |
| [get_Bidi](./get_bidi/)() | يحصل أو يضبط ما إذا كانت هذه الفقرة من اليمين إلى اليسار. |
| [get_Borders](./get_borders/)() | يحصل على مجموعة حدود الفقرة. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | يحصل أو يضبط القيمة (بالحروف) للمسافة البادئة للسطر الأول أو المعلقة. استخدم القيم الموجبة لضبط مسافة البادئة للسطر الأول، والقيم السالبة لضبط المسافة المعلقة. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | يحصل أو يضبط قيمة المسافة البادئة اليسرى (بالحروف) للفقرات المحددة. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | يحصل أو يضبط قيمة المسافة البادئة اليمنى (بالحروف) للفقرات المحددة. |
| [get_DropCapPosition](./get_dropcapposition/)() | يحصل أو يضبط موضع النص بالحرف الأول الكبير. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | يحصل أو يضبط علامة تشير إلى ما إذا كانت قواعد كسر السطر للشرق الآسيوي مطبقة على الفقرة الحالية. |
| [get_FirstLineIndent](./get_firstlineindent/)() | يحصل أو يضبط القيمة (بالنقاط) للمسافة البادئة للسطر الأول أو المعلقة. استخدم القيم الموجبة لضبط مسافة البادئة للسطر الأول، والقيم السالبة لضبط المسافة المعلقة. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | يحصل أو يضبط علامة تشير إلى ما إذا كانت علامات الترقيم المعلقة مفعلة للفقرة الحالية. |
| [get_IsHeading](./get_isheading/)() | صحيح عندما يكون نمط الفقرة أحد أنماط العناوين المدمجة. |
| [get_IsListItem](./get_islistitem/)() | صحيح عندما تكون الفقرة عنصرًا في قائمة نقطية أو مرقمة. |
| [get_KeepTogether](./get_keeptogether/)() | صحيح إذا كان يجب أن تبقى جميع الأسطر في الفقرة على نفس الصفحة. |
| [get_KeepWithNext](./get_keepwithnext/)() | صحيح إذا كان يجب أن تبقى الفقرة على نفس الصفحة مع الفقرة التي تليها. |
| [get_LeftIndent](./get_leftindent/)() | يحصل أو يضبط القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة. |
| [get_LineSpacing](./get_linespacing/)() | يحصل أو يضبط تباعد السطر (بالنقاط) للفقرة. |
| [get_LineSpacingRule](./get_linespacingrule/)() | يحصل أو يضبط تباعد السطر للفقرة. |
| [get_LinesToDrop](./get_linestodrop/)() | يحصل أو يضبط عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير. |
| [get_LineUnitAfter](./get_lineunitafter/)() | يحصل أو يضبط مقدار التباعد (بخطوط الشبكة) بعد الفقرات. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | يحصل أو يضبط مقدار التباعد (بخطوط الشبكة) قبل الفقرات. |
| [get_MirrorIndents](./get_mirrorindents/)() | يحصل أو يضبط علامة تشير إلى ما إذا كانت المسافات البادئة اليسرى واليمنى ذات عرض متساوٍ. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | عند **true**، سيتم تجاهل [SpaceBefore](./get_spacebefore/) و[SpaceAfter](./get_spaceafter/) بين الفقرات ذات النمط نفسه. |
| [get_OutlineLevel](./get_outlinelevel/)() | يحدد مستوى المخطط للفقرة في المستند. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | صحيح إذا تم فرض فاصل صفحة قبل الفقرة. |
| [get_RightIndent](./get_rightindent/)() | يحصل أو يعيّن القيمة (بالنقاط) التي تمثل المسافة البادئة اليمنى للفقرة. |
| [get_Shading](./get_shading/)() | يرجع كائنًا [Shading](../shading/) يشير إلى تنسيق التظليل للفقرة. |
| [get_SnapToGrid](./get_snaptogrid/)() | يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتوى في الفقرة. |
| [get_SpaceAfter](./get_spaceafter/)() | يحصل أو يعيّن مقدار المسافة (بالنقاط) بعد الفقرة. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا. |
| [get_SpaceBefore](./get_spacebefore/)() | يحصل أو يعيّن مقدار المسافة (بالنقاط) قبل الفقرة. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | صحيح إذا تم تعيين مقدار المسافة قبل الفقرة تلقائيًا. |
| [get_Style](./get_style/)() | يحصل أو يعيّن نمط الفقرة المطبق على هذا التنسيق. |
| [get_StyleIdentifier](./get_styleidentifier/)() | يحصل أو يعيّن معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق. |
| [get_StyleName](./get_stylename/)() | يحصل أو يعيّن اسم نمط الفقرة المطبق على هذا التنسيق. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | يحدد ما إذا كان يجب استثناء الفقرة الحالية من أي تجزئة تُطبق في إعدادات المستند. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | يحدد ما إذا كان يجب استثناء أسطر الفقرة الحالية من ترقيم الأسطر الذي يُطبق في القسم الأب. |
| [get_TabStops](./get_tabstops/)() | يحصل على مجموعة نقاط التبويب المخصصة المعرفة لهذا الكائن. |
| [get_WidowControl](./get_widowcontrol/)() | صحيح إذا كان يجب أن تبقى السطران الأول والأخير في الفقرة على نفس الصفحة مع باقي الفقرة. |
| [get_WordWrap](./get_wordwrap/)() | إذا كانت هذه الخاصية **false**، يمكن لف النص اللاتيني في وسط كلمة للفقرة الحالية. وإلا يتم لف النص اللاتيني بالكلمات الكاملة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | محدد للخاصية [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | معين لـ [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | معين لـ [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | معين لـ [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | معين لـ [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | معين لـ [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | معين لـ [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | معين لـ [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | معين لـ [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية إنشاء مستند Aspose.Words يدويًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يحتوي مستند فارغ على قسم واحد، جسم واحد وفقرة واحدة.
// استدعِ طريقة "RemoveAllChildren" لإزالة جميع تلك العقد،
// وانتهي إلى عقدة مستند بدون أي أبناء.
doc->RemoveAllChildren();

// ليس لهذا المستند الآن أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديلها، سنحتاج إلى إعادة ملء مجموعة العقد الخاصة بها.
// أولاً، أنشئ قسمًا جديدًا، ثم أضفه كطفل إلى عقدة المستند الجذرية.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// حدد بعض خصائص إعداد الصفحة للقسم.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// يحتاج القسم إلى جسم، سيحتوي ويعرض جميع محتوياته
// على الصفحة بين رأس وتذييل القسم.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// أنشئ فقرة، واضبط بعض خصائص التنسيق، ثم أضفها كعنصر فرعي إلى الجسم.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// أخيرًا، أضف بعض المحتوى لإنشاء المستند. أنشئ عنصر Run،
// اضبط مظهره ومحتوياته، ثم أضفه كعنصر فرعي إلى الفقرة.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
