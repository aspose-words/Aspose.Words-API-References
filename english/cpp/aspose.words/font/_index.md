---
title: Aspose::Words::Font class
linktitle: Font
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font class. Contains font attributes (font name, font size, color, and so on) for an object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words/font/
---
## Font class


Contains font attributes (font name, font size, color, and so on) for an object. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets to default font formatting. |
| [get_AllCaps](./get_allcaps/)() | True if the font is formatted as all capital letters. |
| [get_AutoColor](./get_autocolor/)() | Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | Specifies whether the contents of this run shall have right-to-left characteristics. |
| [get_Bold](./get_bold/)() | True if the font is formatted as bold. |
| [get_BoldBi](./get_boldbi/)() | True if the right-to-left text is formatted as bold. |
| [get_Border](./get_border/)() | Returns a [Border](../border/) object that specifies border for the font. |
| [get_Color](./get_color/)() | Gets or sets the color of the font. |
| [get_ComplexScript](./get_complexscript/)() | Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | True if the font is formatted as double strikethrough text. |
| [get_Emboss](./get_emboss/)() | True if the font is formatted as embossed. |
| [get_EmphasisMark](./get_emphasismark/)() | Gets or sets the emphasis mark applied to this formatting. |
| [get_Engrave](./get_engrave/)() | True if the font is formatted as engraved. |
| [get_Fill](./get_fill/)() | Gets fill formatting for the [Font](./). |
| [get_Hidden](./get_hidden/)() | True if the font is formatted as hidden text. |
| [get_HighlightColor](./get_highlightcolor/)() | Gets or sets the highlight (marker) color. |
| [get_Italic](./get_italic/)() | True if the font is formatted as italic. |
| [get_ItalicBi](./get_italicbi/)() | True if the right-to-left text is formatted as italic. |
| [get_Kerning](./get_kerning/)() | Gets or sets the font size at which kerning starts. |
| [get_LineSpacing](./get_linespacing/)() | Returns line spacing of this font (in points). |
| [get_LocaleId](./get_localeid/)() | Gets or sets the locale identifier (language) of the formatted characters. |
| [get_LocaleIdBi](./get_localeidbi/)() | Gets or sets the locale identifier (language) of the formatted right-to-left characters. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Gets or sets the locale identifier (language) of the formatted Asian characters. |
| [get_Name](./get_name/)() | Gets or sets the name of the font. |
| [get_NameAscii](./get_nameascii/)() | Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127). |
| [get_NameBi](./get_namebi/)() | Returns or sets the name of the font in a right-to-left language document. |
| [get_NameFarEast](./get_namefareast/)() | Returns or sets an East Asian font name. |
| [get_NameOther](./get_nameother/)() | Returns or sets the font used for characters with character codes from 128 through 255. |
| [get_NoProofing](./get_noproofing/)() | True when the formatted characters are not to be spell checked. |
| [get_NumberSpacing](./get_numberspacing/)() | Gets the spacing type of the numeral being displayed. |
| [get_Outline](./get_outline/)() | True if the font is formatted as outline. |
| [get_Position](./get_position/)() | Gets or sets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it. |
| [get_Scaling](./get_scaling/)() | Gets or sets character width scaling in percent. |
| [get_Shading](./get_shading/)() | Returns a [Shading](../shading/) object that refers to the shading formatting for the font. |
| [get_Shadow](./get_shadow/)() | True if the font is formatted as shadowed. |
| [get_Size](./get_size/)() | Gets or sets the font size in points. |
| [get_SizeBi](./get_sizebi/)() | Gets or sets the font size in points used in a right-to-left document. |
| [get_SmallCaps](./get_smallcaps/)() | True if the font is formatted as small capital letters. |
| [get_SnapToGrid](./get_snaptogrid/)() | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [get_Spacing](./get_spacing/)() | Returns or sets the spacing (in points) between characters . |
| [get_StrikeThrough](./get_strikethrough/)() | True if the font is formatted as strikethrough text. |
| [get_Style](./get_style/)() | Gets or sets the character style applied to this formatting. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Gets or sets the locale independent style identifier of the character style applied to this formatting. |
| [get_StyleName](./get_stylename/)() | Gets or sets the name of the character style applied to this formatting. |
| [get_Subscript](./get_subscript/)() | True if the font is formatted as subscript. |
| [get_Superscript](./get_superscript/)() | True if the font is formatted as superscript. |
| [get_TextEffect](./get_texteffect/)() | Gets or sets the font animation effect. |
| [get_ThemeColor](./get_themecolor/)() | Gets or sets the theme color in the applied color scheme that is associated with this [Font](./) object. |
| [get_ThemeFont](./get_themefont/)() | Gets or sets the theme font in the applied font scheme that is associated with this [Font](./) object. |
| [get_ThemeFontAscii](./get_themefontascii/)() | Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](./) object. |
| [get_ThemeFontBi](./get_themefontbi/)() | Gets or sets the theme font in the applied font scheme that is associated with this [Font](./) object in a right-to-left language document. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Gets or sets the East Asian theme font in the applied font scheme that is associated with this [Font](./) object. |
| [get_ThemeFontOther](./get_themefontother/)() | Gets or sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](./) object. |
| [get_TintAndShade](./get_tintandshade/)() | Gets or sets a double value that lightens or darkens a color. |
| [get_Underline](./get_underline/)() | Gets or sets the type of underline applied to the font. |
| [get_UnderlineColor](./get_underlinecolor/)() | Gets or sets the color of the underline applied to the font. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Checks if particular DrawingML text effect is applied. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Setter for [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Setter for [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Setter for [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Setter for [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Setter for [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Setter for [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Setter for [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Setter for [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Setter for [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Setter for [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Setter for [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Setter for [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Setter for [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Setter for [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Setter for [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Setter for [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Setter for [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Setter for [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Setter for [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Setter for [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Setter for [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Sets the spacing type of the numeral being displayed. |
| [set_Outline](./set_outline/)(bool) | Setter for [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Setter for [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Setter for [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Setter for [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Setter for [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Setter for [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Setter for [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [set_Spacing](./set_spacing/)(double) | Setter for [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Setter for [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter for [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Setter for [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter for [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Setter for [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Setter for [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Setter for [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Setter for [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Setter for [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Setter for [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Setter for [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Setter for [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Setter for [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Setter for [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Setter for [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Remarks


You do not create instances of the [Font](./) class directly. You just use [Font](./) to access the font properties of the various objects such as [Run](../run/), [Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).

## Examples



Shows how to insert a string surrounded by a border into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(ArtifactsDir + u"Border.FontBorder.docx");
```


Shows how to format a run of text using its font property. 
```cpp
auto doc = MakeObject<Document>();
auto run = MakeObject<Run>(doc, u"Hello world!");

SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(run);
doc->Save(ArtifactsDir + u"Font.CreateFormattedRun.docx");
```


Shows how to create and use a paragraph style with list formatting. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a custom paragraph style.
SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Create a list and make sure the paragraphs that use this style will use this list.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(ArtifactsDir + u"Styles.ParagraphStyleBulletedList.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
