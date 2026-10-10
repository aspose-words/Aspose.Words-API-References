---
title: "Aspose::Words::Font sınıfı"
linktitle: "Font"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font sınıfı. Bir nesne için yazı tipi özelliklerini (yazı tipi adı, yazı tipi boyutu, renk vb.) içerir. Daha fazla bilgi edinmek için C++'daki belgeler makalesini ziyaret edin."
type: docs
weight: 29000
url: /tr/cpp/aspose.words/font/
---
## Font class


Bir nesne için yazı tipi özelliklerini (yazı tipi adı, yazı tipi boyutu, renk vb.) içerir. Daha fazla bilgi edinmek için [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Varsayılan yazı tipi biçimlendirmesini sıfırlar. |
| [get_AllCaps](./get_allcaps/)() | Yazı tipi tüm büyük harflerle biçimlendirilmişse doğru. |
| [get_AutoColor](./get_autocolor/)() | Metnin mevcut hesaplanmış rengini (siyah veya beyaz) 'otomatik renk' için döndürür. Renk 'otomatik' değilse [Color](./get_color/) döndürür. |
| [get_Bidi](./get_bidi/)() | Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir. |
| [get_Bold](./get_bold/)() | Yazı tipi kalın olarak biçimlendirilmişse doğru. |
| [get_BoldBi](./get_boldbi/)() | Sağdan sola metin kalın olarak biçimlendirilmişse doğru. |
| [get_Border](./get_border/)() | Yazı tipi için kenarlık belirten bir [Border](../border/) nesnesi döndürür. |
| [get_Color](./get_color/)() | Yazı tipinin rengini alır veya ayarlar. |
| [get_ComplexScript](./get_complexscript/)() | Bu çalışmanın biçimlendirmesini belirlerken, içeriğin Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | Yazı tipi çift üstü çizili olarak biçimlendirilmişse doğru. |
| [get_Emboss](./get_emboss/)() | Yazı tipi kabartmalı olarak biçimlendirilmişse doğru. |
| [get_EmphasisMark](./get_emphasismark/)() | Bu biçimlendirmeye uygulanan vurgu işaretini alır veya ayarlar. |
| [get_Engrave](./get_engrave/)() | Yazı tipi oyma olarak biçimlendirilmişse doğru. |
| [get_Fill](./get_fill/)() | [Font](./) için dolgu biçimlendirmesini alır. |
| [get_Hidden](./get_hidden/)() | Yazı tipi gizli metin olarak biçimlendirilmişse doğru. |
| [get_HighlightColor](./get_highlightcolor/)() | Vurgulama (işaretleyici) rengini alır veya ayarlar. |
| [get_Italic](./get_italic/)() | Yazı tipi italik olarak biçimlendirilmişse Doğru. |
| [get_ItalicBi](./get_italicbi/)() | Sağdan sola metin italik olarak biçimlendirilmişse doğru. |
| [get_Kerning](./get_kerning/)() | Kerning'in başladığı yazı tipi boyutunu alır veya ayarlar. |
| [get_LineSpacing](./get_linespacing/)() | Bu yazı tipinin satır aralığını (puan cinsinden) döndürür. |
| [get_LocaleId](./get_localeid/)() | Biçimlendirilmiş karakterlerin yerel kimliğini (dil) alır veya ayarlar. |
| [get_LocaleIdBi](./get_localeidbi/)() | Biçimlendirilmiş sağdan sola karakterlerin yerel kimliğini (dil) alır veya ayarlar. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Biçimlendirilmiş Asya karakterlerinin yerel kimliğini (dil) alır veya ayarlar. |
| [get_Name](./get_name/)() | Yazı tipinin adını alır veya ayarlar. |
| [get_NameAscii](./get_nameascii/)() | Latin metin (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler) için kullanılan yazı tipini alır veya ayarlar. |
| [get_NameBi](./get_namebi/)() | Sağdan sola dil belgesindeki yazı tipinin adını alır veya ayarlar. |
| [get_NameFarEast](./get_namefareast/)() | Doğu Asya yazı tipi adını alır veya ayarlar. |
| [get_NameOther](./get_nameother/)() | 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar. |
| [get_NoProofing](./get_noproofing/)() | Biçimlendirilmiş karakterlerin imla denetimi yapılmaması gerektiğinde doğrudur. |
| [get_NumberSpacing](./get_numberspacing/)() | Görüntülenen sayının boşluk tipini alır veya ayarlar. |
| [get_Outline](./get_outline/)() | Yazı tipi taslak olarak biçimlendirilmişse doğrudur. |
| [get_Position](./get_position/)() | Metnin (puan cinsinden) temel çizgiye göre konumunu alır veya ayarlar. Pozitif bir sayı metni yükseltir, negatif bir sayı ise alçaltır. |
| [get_Scaling](./get_scaling/)() | Karakter genişliği ölçeklendirmesini yüzde olarak alır veya ayarlar. |
| [get_Shading](./get_shading/)() | Yazı tipi için gölgelendirme biçimlendirmesine referans veren bir [Shading](../shading/) nesnesi döndürür. |
| [get_Shadow](./get_shadow/)() | Yazı tipi gölgeli olarak biçimlendirilmişse doğrudur. |
| [get_Size](./get_size/)() | Yazı tipi boyutunu puan cinsinden alır veya ayarlar. |
| [get_SizeBi](./get_sizebi/)() | Sağdan sola belge içinde kullanılan yazı tipi boyutunu puan cinsinden alır veya ayarlar. |
| [get_SmallCaps](./get_smallcaps/)() | Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur. |
| [get_SnapToGrid](./get_snaptogrid/)() | Geçerli yazı tipinin yerleşim sırasında belge ızgarasındaki satır başına karakter ayarlarını kullanıp kullanmayacağını belirtir. |
| [get_Spacing](./get_spacing/)() | Karakterler arasındaki boşluğu (puan cinsinden) döndürür veya ayarlar. |
| [get_StrikeThrough](./get_strikethrough/)() | Yazı tipi üzeri çizili metin olarak biçimlendirilmişse doğrudur. |
| [get_Style](./get_style/)() | Bu biçimlendirmeye uygulanan karakter stilini alır veya ayarlar. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını alır veya ayarlar. |
| [get_StyleName](./get_stylename/)() | Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar. |
| [get_Subscript](./get_subscript/)() | Yazı tipi alt simge olarak biçimlendirilmişse doğrudur. |
| [get_Superscript](./get_superscript/)() | Yazı tipi üst simge olarak biçimlendirilmişse doğrudur. |
| [get_TextEffect](./get_texteffect/)() | Yazı tipi animasyon etkisini alır veya ayarlar. |
| [get_ThemeColor](./get_themecolor/)() | Bu [Font](./) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır veya ayarlar. |
| [get_ThemeFont](./get_themefont/)() | Bu [Font](./) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır veya ayarlar. |
| [get_ThemeFontAscii](./get_themefontascii/)() | Bu [Font](./) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metni (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler) için kullanılan tema yazı tipini alır veya ayarlar. |
| [get_ThemeFontBi](./get_themefontbi/)() | Sağdan sola dil belgesinde bu [Font](./) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır veya ayarlar. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Bu [Font](./) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipini alır veya ayarlar. |
| [get_ThemeFontOther](./get_themefontother/)() | Bu [Font](./) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipini alır veya ayarlar. |
| [get_TintAndShade](./get_tintandshade/)() | Bir rengi açan veya karartan çift bir değeri alır veya ayarlar. |
| [get_Underline](./get_underline/)() | Yazı tipine uygulanan alt çizgi türünü alır veya ayarlar. |
| [get_UnderlineColor](./get_underlinecolor/)() | Yazı tipine uygulanan alt çizgi rengini alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Belirli bir DrawingML metin efektinin uygulanıp uygulanmadığını kontrol eder. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | [Aspose::Words::Font::get_AllCaps](./get_allcaps/) için ayarlayıcı. |
| [set_Bidi](./set_bidi/)(bool) | [Aspose::Words::Font::get_Bidi](./get_bidi/) için ayarlayıcı. |
| [set_Bold](./set_bold/)(bool) | [Aspose::Words::Font::get_Bold](./get_bold/) için ayarlayıcı. |
| [set_BoldBi](./set_boldbi/)(bool) | [Aspose::Words::Font::get_BoldBi](./get_boldbi/) için ayarlayıcı. |
| [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::Font::get_Color](./get_color/) için ayarlayıcı. |
| [set_ComplexScript](./set_complexscript/)(bool) | [Aspose::Words::Font::get_ComplexScript](./get_complexscript/) için ayarlayıcı. |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/) için ayarlayıcı. |
| [set_Emboss](./set_emboss/)(bool) | [Aspose::Words::Font::get_Emboss](./get_emboss/) için ayarlayıcı. |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/) için ayarlayıcı. |
| [set_Engrave](./set_engrave/)(bool) | [Aspose::Words::Font::get_Engrave](./get_engrave/) için ayarlayıcı. |
| [set_Hidden](./set_hidden/)(bool) | [Aspose::Words::Font::get_Hidden](./get_hidden/) için ayarlayıcı. |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/) için ayarlayıcı. |
| [set_Italic](./set_italic/)(bool) | [Aspose::Words::Font::get_Italic](./get_italic/) için ayarlayıcı. |
| [set_ItalicBi](./set_italicbi/)(bool) | [Aspose::Words::Font::get_ItalicBi](./get_italicbi/) için ayarlayıcı. |
| [set_Kerning](./set_kerning/)(double) | [Aspose::Words::Font::get_Kerning](./get_kerning/) için ayarlayıcı. |
| [set_LocaleId](./set_localeid/)(int32_t) | [Aspose::Words::Font::get_LocaleId](./get_localeid/) için ayarlayıcı. |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/) için ayarlayıcı. |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/) için ayarlayıcı. |
| [set_Name](./set_name/)(const System::String\&) | [Aspose::Words::Font::get_Name](./get_name/) için ayarlayıcı. |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | [Aspose::Words::Font::get_NameAscii](./get_nameascii/) için ayarlayıcı. |
| [set_NameBi](./set_namebi/)(const System::String\&) | [Aspose::Words::Font::get_NameBi](./get_namebi/) için ayarlayıcı. |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Ayarlayıcı [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Ayarlayıcı [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Ayarlayıcı [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Ayarlayıcı [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Ayarlayıcı [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Geçerli yazı tipinin yerleşim sırasında belge ızgarasındaki satır başına karakter ayarlarını kullanıp kullanmayacağını belirtir. |
| [set_Spacing](./set_spacing/)(double) | Ayarlayıcı [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Ayarlayıcı [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Ayarlayıcı [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Ayarlayıcı [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Ayarlayıcı [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Ayarlayıcı [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Ayarlayıcı [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Ayarlayıcı [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Ayarlayıcı [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Ayarlayıcı [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Ayarlayıcı [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Ayarlayıcı [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Ayarlayıcı [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Açıklamalar


Doğrudan [Font](./) sınıfının örneklerini oluşturmazsınız. Sadece [Font](./) sınıfını, [Run](../run/), [Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/) gibi çeşitli nesnelerin yazı tipi özelliklerine erişmek için kullanırsınız.

## Örnekler



Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Bir metin run'ını font özelliğini kullanarak nasıl biçimlendireceğini gösterir.
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


Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulup kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Özel bir paragraf stili oluştur.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Bir liste oluşturun ve bu stili kullanan paragrafların bu listeyi kullanmasını sağlayın.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Paragraf stilini belge oluşturucunun mevcut paragrafına uygulayın ve ardından metin ekleyin.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stile değiştirin ve başka bir paragraf yazın.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
