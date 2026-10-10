---
title: "Aspose::Words::ParagraphFormat class"
linktitle: "ParagraphFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat sınıfı. Bir paragrafın tüm biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 49000
url: /tr/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Bir paragrafın tüm biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için, [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) dokümantasyon makalesini ziyaret edin.

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Paragraf biçimlendirmesini varsayılan ayarlara sıfırlar. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Geçerli paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmayacağını gösteren bir bayrağı alır veya ayarlar. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Geçerli paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmayacağını gösteren bir bayrağı alır veya ayarlar. |
| [get_Alignment](./get_alignment/)() | Paragraf için metin hizalamasını alır veya ayarlar. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Bir satırdaki yazı tiplerinin dikey konumunu alır veya ayarlar. |
| [get_Bidi](./get_bidi/)() | Bunun sağdan sola bir paragraf olup olmadığını alır veya ayarlar. |
| [get_Borders](./get_borders/)() | Paragrafın kenarlık koleksiyonunu alır. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | İlk satır veya sarkıt girinti için değeri (karakter cinsinden) alır veya ayarlar. İlk satır girintisini ayarlamak için pozitif değerleri, sarkıt girintisini ayarlamak için negatif değerleri kullanın. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) alır veya ayarlar. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Belirtilen paragraflar için sağ girinti değerini (karakter cinsinden) alır veya ayarlar. |
| [get_DropCapPosition](./get_dropcapposition/)() | Büyük harf (drop cap) metni için konumu alır veya ayarlar. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Doğu Asya satır sonlandırma kurallarının geçerli paragraf için uygulanıp uygulanmadığını gösteren bayrağı alır veya ayarlar. |
| [get_FirstLineIndent](./get_firstlineindent/)() | İlk satır veya sarkıt girinti için değeri (puan cinsinden) alır veya ayarlar. İlk satır girintisini ayarlamak için pozitif değerleri, sarkıt girintisini ayarlamak için negatif değerleri kullanın. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Geçerli paragrafta sarkıt noktalama işaretlerinin etkin olup olmadığını gösteren bayrağı alır veya ayarlar. |
| [get_IsHeading](./get_isheading/)() | True, paragraf stili yerleşik Başlık stillerinden biri olduğunda. |
| [get_IsListItem](./get_islistitem/)() | True, paragraf madde işaretli veya numaralı bir listedeki öğe olduğunda. |
| [get_KeepTogether](./get_keeptogether/)() | True, paragraftaki tüm satırların aynı sayfada kalması gerektiğinde. |
| [get_KeepWithNext](./get_keepwithnext/)() | True, paragrafın ardından gelen paragrafla aynı sayfada kalması gerektiğinde. |
| [get_LeftIndent](./get_leftindent/)() | Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) alır veya ayarlar. |
| [get_LineSpacing](./get_linespacing/)() | Paragraf için satır aralığını (puan cinsinden) alır veya ayarlar. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Paragraf için satır aralığını alır veya ayarlar. |
| [get_LinesToDrop](./get_linestodrop/)() | Büyük harf yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını alır veya ayarlar. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Paragraflardan sonraki boşluk miktarını (ızgara satırı cinsinden) alır veya ayarlar. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Paragraflardan önceki boşluk miktarını (ızgara satırı cinsinden) alır veya ayarlar. |
| [get_MirrorIndents](./get_mirrorindents/)() | Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bayrağı alır veya ayarlar. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | When **true**, [SpaceBefore](./get_spacebefore/) ve [SpaceAfter](./get_spaceafter/) aynı stilin paragrafları arasında yok sayılacaktır. |
| [get_OutlineLevel](./get_outlinelevel/)() | Belgedeki paragrafın anahat seviyesini belirtir. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | True, paragraftan önce bir sayfa sonu zorlanıyorsa. |
| [get_RightIndent](./get_rightindent/)() | Paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) alır veya ayarlar. |
| [get_Shading](./get_shading/)() | Paragrafın gölgelendirme biçimlendirmesine referans veren bir [Shading](../shading/) nesnesi döndürür. |
| [get_SnapToGrid](./get_snaptogrid/)() | Geçerli paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara çizgileri ayarlarını kullanıp kullanmayacağını belirtir. |
| [get_SpaceAfter](./get_spaceafter/)() | Paragraftan sonraki boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | Paragraftan sonraki boşluk miktarı otomatik olarak ayarlanmışsa doğru. |
| [get_SpaceBefore](./get_spacebefore/)() | Paragraftan önceki boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | Paragraftan önceki boşluk miktarı otomatik olarak ayarlanmışsa doğru. |
| [get_Style](./get_style/)() | Bu biçimlendirmeye uygulanan paragraf stilini alır veya ayarlar. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Bu biçimlendirmeye uygulanan paragraf stilinin yerel bağımsız stil tanımlayıcısını alır veya ayarlar. |
| [get_StyleName](./get_stylename/)() | Bu biçimlendirmeye uygulanan paragraf stilinin adını alır veya ayarlar. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir hecelemeden muaf olup olmayacağını belirtir. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Geçerli paragrafın satırlarının, üst bölümde uygulanan satır numaralandırmasından muaf olup olmayacağını belirtir. |
| [get_TabStops](./get_tabstops/)() | Bu nesne için tanımlanan özel sekme durakları koleksiyonunu alır. |
| [get_WidowControl](./get_widowcontrol/)() | Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması gerekiyorsa doğru. |
| [get_WordWrap](./get_wordwrap/)() | Bu özellik **false** ise, kelimenin ortasındaki Latin metni geçerli paragrafta kaydırılabilir. Aksi takdirde Latin metni bütün kelimeler halinde kaydırılır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/) için ayarlayıcı. |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/) için ayarlayıcı. |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/) için ayarlayıcı. |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/) için ayarlayıcı. |
| [set_Bidi](./set_bidi/)(bool) | [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/) için ayarlayıcı. |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/) için ayarlayıcı. |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/) için ayarlayıcı. |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/) için ayarlayıcı. |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/) için ayarlayıcı. |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/) için ayarlayıcı. |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Ayarlayıcı [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Örnekler



Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// "RemoveAllChildren" yöntemini çağırarak bu düğümlerin tümünü kaldırın,
// ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc->RemoveAllChildren();

// Bu belge artık içerik ekleyebileceğimiz birleşik alt düğümlere sahip değil.
// Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// İlk olarak yeni bir bölüm oluşturun ve ardından kök belge düğümüne çocuk olarak ekleyin.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Bölüm için bazı sayfa ayarı özelliklerini ayarlayın.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Bir bölüm bir gövdeye ihtiyaç duyar, bu gövde tüm içeriğini barındırır ve gösterir
// sayfada bölümün başlığı ile altbilgisi arasındaki alanda.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu gövdenin bir çocuğu olarak ekleyin.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Son olarak, belgeye içerik ekleyin. Bir run oluşturun,
// Görünümünü ve içeriğini ayarlayın, ardından onu paragrafın bir çocuğu olarak ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
