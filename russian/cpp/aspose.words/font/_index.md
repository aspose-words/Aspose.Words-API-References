---
title: "Aspose::Words::Font class"
linktitle: "Font"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font class. Содержит атрибуты шрифта (название шрифта, размер, цвет и т.д.) для объекта. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words/font/
---
## Font class


Содержит атрибуты шрифта (название шрифта, размер шрифта, цвет и т.д.) для объекта. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Сбрасывает форматирование шрифта к значениям по умолчанию. |
| [get_AllCaps](./get_allcaps/)() | Истина, если шрифт отформатирован как все заглавные буквы. |
| [get_AutoColor](./get_autocolor/)() | Возвращает текущий вычисленный цвет текста (чёрный или белый), используемый для «auto color». Если цвет не «auto», то возвращает [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | Указывает, должны ли содержимое этого фрагмента иметь свойства справа налево. |
| [get_Bold](./get_bold/)() | True, если шрифт оформлен как полужирный. |
| [get_BoldBi](./get_boldbi/)() | Истина, если текст справа налево отформатирован полужирным. |
| [get_Border](./get_border/)() | Возвращает объект [Border](../border/), который задаёт границу для шрифта. |
| [get_Color](./get_color/)() | Получает или задаёт цвет шрифта. |
| [get_ComplexScript](./get_complexscript/)() | Указывает, следует ли рассматривать содержимое этого фрагмента как текст сложного сценария независимо от их значений Unicode при определении форматирования этого фрагмента. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | Истина, если шрифт отформатирован как двойное зачеркивание. |
| [get_Emboss](./get_emboss/)() | Истина, если шрифт отформатирован как рельефный. |
| [get_EmphasisMark](./get_emphasismark/)() | Получает или задаёт знак акцента, применяемый к этому форматированию. |
| [get_Engrave](./get_engrave/)() | Истина, если шрифт отформатирован как гравированный. |
| [get_Fill](./get_fill/)() | Получает формат заполнения для [Font](./). |
| [get_Hidden](./get_hidden/)() | Истина, если шрифт отформатирован как скрытый текст. |
| [get_HighlightColor](./get_highlightcolor/)() | Получает или задаёт цвет выделения (маркер). |
| [get_Italic](./get_italic/)() | True, если шрифт оформлен курсивом. |
| [get_ItalicBi](./get_italicbi/)() | Истина, если текст справа налево отформатирован курсивом. |
| [get_Kerning](./get_kerning/)() | Получает или задаёт размер шрифта, с которого начинается кернинг. |
| [get_LineSpacing](./get_linespacing/)() | Возвращает межстрочный интервал этого шрифта (в пунктах). |
| [get_LocaleId](./get_localeid/)() | Получает или задаёт идентификатор локали (язык) отформатированных символов. |
| [get_LocaleIdBi](./get_localeidbi/)() | Получает или задаёт идентификатор локали (язык) отформатированных символов справа налево. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Получает или задаёт идентификатор локали (язык) отформатированных азиатских символов. |
| [get_Name](./get_name/)() | Получает или задаёт название шрифта. |
| [get_NameAscii](./get_nameascii/)() | Возвращает или задаёт шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |
| [get_NameBi](./get_namebi/)() | Возвращает или задаёт название шрифта в документе на языке с направлением справа налево. |
| [get_NameFarEast](./get_namefareast/)() | Возвращает или задаёт название восточноазиатского шрифта. |
| [get_NameOther](./get_nameother/)() | Возвращает или задает шрифт, используемый для символов с кодами от 128 до 255. |
| [get_NoProofing](./get_noproofing/)() | Истина, когда отформатированные символы не подлежат проверке орфографии. |
| [get_NumberSpacing](./get_numberspacing/)() | Получает или задает тип интервала цифры, отображаемой. |
| [get_Outline](./get_outline/)() | Истина, если шрифт отформатирован как контур. |
| [get_Position](./get_position/)() | Получает или задает позицию текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, а отрицательное опускает его. |
| [get_Scaling](./get_scaling/)() | Получает или задает масштабирование ширины символов в процентах. |
| [get_Shading](./get_shading/)() | Возвращает объект [Shading](../shading/), который ссылается на форматирование затенения для шрифта. |
| [get_Shadow](./get_shadow/)() | Истина, если шрифт отформатирован как с тенью. |
| [get_Size](./get_size/)() | Получает или задает размер шрифта в пунктах. |
| [get_SizeBi](./get_sizebi/)() | Получает или задает размер шрифта в пунктах, используемый в документе с направлением справа налево. |
| [get_SmallCaps](./get_smallcaps/)() | Истина, если шрифт отформатирован как малые заглавные буквы. |
| [get_SnapToGrid](./get_snaptogrid/)() | Указывает, следует ли текущему шрифту использовать настройки сетки документа «символов в строке» при размещении. |
| [get_Spacing](./get_spacing/)() | Возвращает или задает интервал (в пунктах) между символами. |
| [get_StrikeThrough](./get_strikethrough/)() | Истина, если шрифт отформатирован как перечёркнутый текст. |
| [get_Style](./get_style/)() | Получает или задает стиль символов, применяемый к этому форматированию. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Получает или задает независимый от локали идентификатор стиля символов, применяемый к этому форматированию. |
| [get_StyleName](./get_stylename/)() | Получает или задает имя стиля символов, применяемого к этому форматированию. |
| [get_Subscript](./get_subscript/)() | Истина, если шрифт отформатирован как нижний индекс. |
| [get_Superscript](./get_superscript/)() | Истина, если шрифт отформатирован как верхний индекс. |
| [get_TextEffect](./get_texteffect/)() | Получает или задает эффект анимации шрифта. |
| [get_ThemeColor](./get_themecolor/)() | Получает или задает цвет темы в применяемой цветовой схеме, связанной с этим объектом [Font](./). |
| [get_ThemeFont](./get_themefont/)() | Получает или задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом [Font](./). |
| [get_ThemeFontAscii](./get_themefontascii/)() | Получает или задает шрифт темы, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом [Font](./). |
| [get_ThemeFontBi](./get_themefontbi/)() | Получает или задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом [Font](./) в документе с языком справа налево. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Получает или задает восточноазиатский шрифт темы в применяемой схеме шрифтов, связанной с этим объектом [Font](./). |
| [get_ThemeFontOther](./get_themefontother/)() | Получает или задает шрифт темы, используемый для символов с кодами от 128 до 255 в применяемой схеме шрифтов, связанной с этим объектом [Font](./). |
| [get_TintAndShade](./get_tintandshade/)() | Получает или задаёт двойное значение, которое осветляет или затемняет цвет. |
| [get_Underline](./get_underline/)() | Получает или задает тип подчеркивания, применяемого к шрифту. |
| [get_UnderlineColor](./get_underlinecolor/)() | Получает или задает цвет подчеркивания, применяемого к шрифту. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Проверяет, применён ли конкретный эффект текста DrawingML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Сеттер для [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Сеттер для [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Сеттер для [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Сеттер для [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Сеттер для [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Сеттер для [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Сеттер для [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Сеттер для [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Сеттер для [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Сеттер для [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Сеттер для [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Сеттер для [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Сеттер для [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Сеттер для [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Сеттер для [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Сеттер для [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Сеттер для [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Сеттер для [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Сеттер для [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Сеттер для [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Сеттер для [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Сеттер для [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Сеттер для [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Сеттер для [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Сеттер для [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Сеттер для [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Сеттер для [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Сеттер для [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Указывает, следует ли текущему шрифту использовать настройки сетки документа «символов в строке» при размещении. |
| [set_Spacing](./set_spacing/)(double) | Сеттер для [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Сеттер для [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Сеттер для [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Сеттер для [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Сеттер для [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Сеттер для [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Сеттер для [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Сеттер для [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Сеттер для [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Сеттер для [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Сеттер для [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Сеттер для [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Сеттер для [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Сеттер для [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Сеттер для [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте экземпляры класса [Font](./) напрямую. Вы просто используете [Font](./) для доступа к свойствам шрифта различных объектов, таких как [Run](../run/), [Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).

## Примеры



Показывает, как вставить строку, окружённую границей, в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Показывает, как форматировать run текста, используя его свойство font.
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


Показывает, как создать и использовать абзацный стиль со списковой разметкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пользовательский абзацный стиль.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Примените абзацный стиль к текущему абзацу DocumentBuilder, а затем добавьте некоторый текст.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Измените стиль DocumentBuilder на такой, который не содержит форматирования списка, и напишите еще один абзац.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
