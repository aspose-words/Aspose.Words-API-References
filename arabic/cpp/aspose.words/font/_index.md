---
title: "Aspose::Words::Font فئة"
linktitle: "Font"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font فئة. يحتوي على سمات الخط (اسم الخط، حجم الخط، اللون، وما إلى ذلك) لكائن. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words/font/
---
## Font class


يحتوي على سمات الخط (اسم الخط، حجم الخط، اللون، وما إلى ذلك) لكائن. لمعرفة المزيد، زر مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يعيد الضبط إلى تنسيق الخط الافتراضي. |
| [get_AllCaps](./get_allcaps/)() | صحيح إذا كان الخط مُنسقًا كحروف كبيرة كلها. |
| [get_AutoColor](./get_autocolor/)() | يعيد اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في 'اللون التلقائي'. إذا لم يكن اللون 'تلقائي' فسيعيد [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | يحدد ما إذا كان محتوى هذا المقطع سيحتوي على خصائص من اليمين إلى اليسار. |
| [get_Bold](./get_bold/)() | صحيح إذا كان الخط مُنسقًا كغامق. |
| [get_BoldBi](./get_boldbi/)() | صحيح إذا كان النص من اليمين إلى اليسار مُنسقًا كعريض. |
| [get_Border](./get_border/)() | يعيد كائن [Border](../border/) يحدد الحد للخط. |
| [get_Color](./get_color/)() | يحصل على أو يضبط لون الخط. |
| [get_ComplexScript](./get_complexscript/)() | يحدد ما إذا كان محتوى هذا المقطع سيُعامل كنص كتابة معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | صحيح إذا كان الخط مُنسقًا كنص مع شطب مزدوج. |
| [get_Emboss](./get_emboss/)() | صحيح إذا كان الخط مُنسقًا كمنقوش. |
| [get_EmphasisMark](./get_emphasismark/)() | يحصل على أو يضبط علامة التأكيد المطبقة على هذا التنسيق. |
| [get_Engrave](./get_engrave/)() | صحيح إذا كان الخط مُنسقًا كمنقوش. |
| [get_Fill](./get_fill/)() | يحصل على تنسيق التعبئة للـ [Font](./). |
| [get_Hidden](./get_hidden/)() | صحيح إذا كان الخط مُنسقًا كنص مخفي. |
| [get_HighlightColor](./get_highlightcolor/)() | يحصل على أو يضبط لون التمييز (العلامة). |
| [get_Italic](./get_italic/)() | صحيح إذا كان الخط منسقًا كإيطالي. |
| [get_ItalicBi](./get_italicbi/)() | صحيح إذا كان النص من اليمين إلى اليسار مُنسقًا كمائل. |
| [get_Kerning](./get_kerning/)() | يحصل على أو يضبط حجم الخط الذي يبدأ عنده التباعد بين الحروف. |
| [get_LineSpacing](./get_linespacing/)() | يعيد تباعد الأسطر لهذا الخط (بالنقاط). |
| [get_LocaleId](./get_localeid/)() | يحصل على أو يضبط معرف الإعداد المحلي (اللغة) للأحرف المُنسقة. |
| [get_LocaleIdBi](./get_localeidbi/)() | يحصل على أو يضبط معرف الإعداد المحلي (اللغة) للأحرف المُنسقة من اليمين إلى اليسار. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | يحصل على أو يضبط معرف الإعداد المحلي (اللغة) للأحرف الآسيوية المُنسقة. |
| [get_Name](./get_name/)() | يحصل على أو يضبط اسم الخط. |
| [get_NameAscii](./get_nameascii/)() | يعيد أو يضبط الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127). |
| [get_NameBi](./get_namebi/)() | يعيد أو يضبط اسم الخط في مستند بلغة من اليمين إلى اليسار. |
| [get_NameFarEast](./get_namefareast/)() | يعيد أو يضبط اسم خط آسيوي شرقي. |
| [get_NameOther](./get_nameother/)() | إرجاع أو تعيين الخط المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255. |
| [get_NoProofing](./get_noproofing/)() | صحيح عندما لا يتم تدقيق إملائي للأحرف المنسقة. |
| [get_NumberSpacing](./get_numberspacing/)() | الحصول أو تعيين نوع التباعد للرقم المعروض. |
| [get_Outline](./get_outline/)() | صحيح إذا كان الخط منسقًا كحدود. |
| [get_Position](./get_position/)() | الحصول أو تعيين موضع النص (بالنقاط) بالنسبة إلى الخط الأساسي. الرقم الموجب يرفع النص، والرقم السالب يخفضه. |
| [get_Scaling](./get_scaling/)() | الحصول أو تعيين مقياس عرض الحرف بالنسبة المئوية. |
| [get_Shading](./get_shading/)() | إرجاع كائن [Shading](../shading/) الذي يشير إلى تنسيق التظليل للخط. |
| [get_Shadow](./get_shadow/)() | صحيح إذا كان الخط منسقًا كظل. |
| [get_Size](./get_size/)() | الحصول أو تعيين حجم الخط بالنقاط. |
| [get_SizeBi](./get_sizebi/)() | الحصول أو تعيين حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار. |
| [get_SmallCaps](./get_smallcaps/)() | صحيح إذا كان الخط منسقًا كحروف صغيرة رأسية. |
| [get_SnapToGrid](./get_snaptogrid/)() | يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات عدد الأحرف في السطر لشبكة المستند عند التخطيط. |
| [get_Spacing](./get_spacing/)() | إرجاع أو تعيين التباعد (بالنقاط) بين الأحرف. |
| [get_StrikeThrough](./get_strikethrough/)() | صحيح إذا كان الخط منسقًا كنص مشطوب. |
| [get_Style](./get_style/)() | الحصول أو تعيين نمط الحرف المطبق على هذا التنسيق. |
| [get_StyleIdentifier](./get_styleidentifier/)() | الحصول أو تعيين معرف النمط المستقل عن اللغة لنمط الحرف المطبق على هذا التنسيق. |
| [get_StyleName](./get_stylename/)() | الحصول أو تعيين اسم نمط الحرف المطبق على هذا التنسيق. |
| [get_Subscript](./get_subscript/)() | صحيح إذا كان الخط منسقًا كحرف سفلي. |
| [get_Superscript](./get_superscript/)() | صحيح إذا كان الخط منسقًا كحرف علوي. |
| [get_TextEffect](./get_texteffect/)() | الحصول أو تعيين تأثير حركة الخط. |
| [get_ThemeColor](./get_themecolor/)() | الحصول أو تعيين لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](./). |
| [get_ThemeFont](./get_themefont/)() | الحصول أو تعيين خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](./). |
| [get_ThemeFontAscii](./get_themefontascii/)() | الحصول أو تعيين خط السمة المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127) في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](./). |
| [get_ThemeFontBi](./get_themefontbi/)() | الحصول أو تعيين خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](./) في مستند بلغة من اليمين إلى اليسار. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | الحصول أو تعيين خط السمة للشرق الآسيوي في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](./). |
| [get_ThemeFontOther](./get_themefontother/)() | يحصل أو يضبط خط السمة المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255 في مخطط الخط المطبق المرتبط بهذا الكائن [Font](./) object. |
| [get_TintAndShade](./get_tintandshade/)() | يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغمق اللون. |
| [get_Underline](./get_underline/)() | يحصل أو يضبط نوع الخط السفلي المطبق على الخط. |
| [get_UnderlineColor](./get_underlinecolor/)() | يحصل أو يضبط لون الخط السفلي المطبق على الخط. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | يتحقق مما إذا كان تأثير نص DrawingML معين مطبقًا. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | مُعيّن لـ [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | مُعيّن لـ [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | مُعيّن لـ [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | مُعيّن لـ [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | مُعيّن لـ [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | مُعيّن لـ [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | مُعيّن لـ [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | مُعيّن لـ [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | مُعيّن لـ [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات عدد الأحرف في السطر لشبكة المستند عند التخطيط. |
| [set_Spacing](./set_spacing/)(double) | مُعيّن لـ [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | مُعيّن لـ [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | مُعيّن لـ [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | مُعيّن لـ [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | مُعيّن لـ [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | مُعيّن لـ [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | مُعيّن لـ [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | مُعيّن لـ [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | مُعيّن لـ [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | مُعيّن لـ [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | مُعيّن لـ [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | دالة الضبط لـ [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | دالة الضبط لـ [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | دالة الضبط لـ [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## ملاحظات


أنت لا تنشئ كائنات من الفئة [Font](./) مباشرة. بل تستخدم [Font](./) للوصول إلى خصائص الخط في الكائنات المختلفة مثل [Run](../run/)، [Paragraph](../paragraph/)، [Style](../style/)، [DocumentBuilder](../documentbuilder/).

## أمثلة



يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


يوضح كيفية تنسيق مقطع نصي باستخدام خاصية الخط الخاصة به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


يظهر كيفية إنشاء واستخدام نمط فقرة مع تنسيق القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء نمط فقرة مخصص.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// إنشاء قائمة والتأكد من أن الفقرات التي تستخدم هذا النمط ستستخدم هذه القائمة.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// تطبيق نمط الفقرة على الفقرة الحالية لمُنشئ المستند، ثم إضافة بعض النص.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// غيّر نمط مُنشئ المستند إلى نمط لا يحتوي على تنسيق القوائم واكتب فقرة أخرى.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
