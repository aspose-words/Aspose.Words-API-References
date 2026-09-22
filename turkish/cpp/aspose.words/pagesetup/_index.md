---
title: "Aspose::Words::PageSetup sınıfı"
linktitle: "PageSetup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup sınıfı. Bir bölümün sayfa ayarı özelliklerini temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 46000
url: /tr/cpp/aspose.words/pagesetup/
---
## PageSetup class


Bir bölümün sayfa ayarı özelliklerini temsil eder. Daha fazla bilgi edinmek için, [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) dokümantasyon makalesini ziyaret edin.

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Sayfa ayarını varsayılan kağıt boyutu, kenar boşlukları ve yönlendirmeye sıfırlar. |
| [get_Bidi](./get_bidi/)() | Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir. |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Sayfa kenarlığının kesişen metinler ve nesnelerle ilişkili konumunu belirtir. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Sayfa kenarlığının hangi sayfalarda basılacağını belirtir. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Belirtilen sayfa kenarlığının sayfa kenarından mı yoksa çevresindeki metinden mi ölçüldüğünü gösteren bir değeri alır veya ayarlar. |
| [get_Borders](./get_borders/)() | Sayfa kenarlıklarının bir koleksiyonunu alır. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Sayfa kenarlığının alt bilgiyi içerip içermediğini belirtir. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Sayfa kenarlığının üst bilgiyi içerip içermediğini belirtir. |
| [get_BottomMargin](./get_bottommargin/)() | Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi (puan cinsinden) döndürür veya ayarlar. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri alır veya ayarlar. |
| [get_CharactersPerLine](./get_charactersperline/)() | Belge ızgarasındaki satır başına karakter sayısını alır veya ayarlar. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | İlk sayfada farklı bir üst bilgi veya alt bilgi kullanılıyorsa doğru. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Bu bölümde dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar. |
| [get_FirstPageTray](./get_firstpagetray/)() | Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (bin) alır. Değer, uygulamaya (yazıcı) özgüdür. |
| [get_FooterDistance](./get_footerdistance/)() | Alt bilgi ile sayfanın alt kısmı arasındaki mesafeyi (puan cinsinden) alır veya ayarlar. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Bu bölümde dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar. |
| [get_Gutter](./get_gutter/)() | Belge ciltleme için kenara eklenen ekstra boşluk miktarını alır veya ayarlar. |
| [get_HeaderDistance](./get_headerdistance/)() | Üst bilgi ile sayfanın üst kısmı arasındaki mesafeyi (puan cinsinden) alır veya ayarlar. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Belgedeki bölüm başlıklarına uygulanan başlık seviyesi stilini alır veya ayarlar. |
| [get_LayoutMode](./get_layoutmode/)() | Bu bölümün yerleşim modunu alır veya ayarlar. |
| [get_LeftMargin](./get_leftmargin/)() | Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (puan cinsinden) alır veya ayarlar. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Satır numaraları için sayısal artışı alır veya ayarlar. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafeyi alır veya ayarlar. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Satır numaralandırmasının nasıl çalıştığını alır veya ayarlar; yani yeni bir sayfa veya bölümün başında yeniden başlayıp başlamayacağını ya da sürekli devam edip etmeyeceğini. |
| [get_LinesPerPage](./get_linesperpage/)() | Belge ızgarasındaki sayfa başına satır sayısını alır veya ayarlar. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Başlangıç satır numarasını alır veya ayarlar. |
| [get_Margins](./get_margins/)() | Sayfanın önceden ayarlanmış [Margins](../margins/) değerini alır veya ayarlar. |
| [get_MultiplePages](./get_multiplepages/)() const | Birden çok sayfalı belgeler için, belgenin bir kitapçık olarak ciltlenebilmesi için nasıl yazdırıldığını veya oluşturulduğunu alır veya ayarlar. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Belgenin tek ve çift numaralı sayfalar için farklı üst ve alt bilgilere sahip olması durumunda doğru. |
| [get_Orientation](./get_orientation/)() | Sayfanın yönünü alır veya ayarlar. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisini (bin) alır. Değer, uygulamaya (yazıcı) özgüdür. |
| [get_PageHeight](./get_pageheight/)() | Sayfanın yüksekliğini puan cinsinden alır veya ayarlar. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Sayfa numarası biçimini alır veya ayarlar. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Bölümün başlangıç sayfa numarasını alır veya ayarlar. |
| [get_PageWidth](./get_pagewidth/)() | Sayfanın genişliğini nokta cinsinden döndürür veya ayarlar. |
| [get_PaperSize](./get_papersize/)() | Kağıt boyutunu döndürür veya ayarlar. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | True if sayfa numaralandırması bölümün başında yeniden başlıyorsa. |
| [get_RightMargin](./get_rightmargin/)() | Sayfanın sağ kenarı ile gövde metninin sağ sınırı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [get_RtlGutter](./get_rtlgutter/)() | Microsoft Word'ün bölümü sağdan sola ya da soldan sağa dillerine göre oluk (gutter) kullanıp kullanmayacağını alır veya ayarlar. |
| [get_SectionStart](./get_sectionstart/)() | Belirtilen nesne için bölüm sonu tipini döndürür veya ayarlar. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Her kitapçıkta yer alacak sayfa sayısını döndürür veya ayarlar. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | True if dipnotlar, dipnotları bastırmayan bir sonraki bölümün sonunda basılıyorsa. Bastırılan dipnotlar, o bölümdeki dipnotlardan önce basılır. |
| [get_TextColumns](./get_textcolumns/)() | Metin sütunlarını temsil eden bir koleksiyon döndürür. |
| [get_TextOrientation](./get_textorientation/)() | Tüm sayfa için [TextOrientation](./get_textorientation/) belirtmeye izin verir. Varsayılan değer [Horizontal](../textorientation/)'dır. |
| [get_TopMargin](./get_topmargin/)() | Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Bir belge ya da bölümdeki her sayfada metnin dikey hizalamasını döndürür veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | [Aspose::Words::PageSetup::get_Bidi](./get_bidi/) için ayarlayıcı. |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/) için ayarlayıcı. |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/) için ayarlayıcı. |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/) için ayarlayıcı. |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/) için ayarlayıcı. |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/) için ayarlayıcı. |
| [set_BottomMargin](./set_bottommargin/)(double) | [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/) için ayarlayıcı. |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/) için ayarlayıcı. |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/) için ayarlayıcı. |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/) için ayarlayıcı. |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (bin) ayarlar. Değer, uygulamaya (yazıcıya) özgüdür. |
| [set_FooterDistance](./set_footerdistance/)(double) | [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/) için ayarlayıcı. |
| [set_Gutter](./set_gutter/)(double) | [Aspose::Words::PageSetup::get_Gutter](./get_gutter/) için ayarlayıcı. |
| [set_HeaderDistance](./set_headerdistance/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Ayarlayıcı [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Ayarlayıcı [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Ayarlayıcı [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Ayarlayıcı [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Ayarlayıcı [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Ayarlayıcı [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Ayarlayıcı [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Ayarlayıcı [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Ayarlayıcı [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Ayarlayıcı [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisini (bin) ayarlar. Değer, uygulamaya (yazıcı) özgüdür. |
| [set_PageHeight](./set_pageheight/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Ayarlayıcı [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Ayarlayıcı [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Ayarlayıcı [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Ayarlayıcı [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Ayarlayıcı [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Ayarlayıcı [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Ayarlayıcı [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | True if dipnotlar, dipnotları bastırmayan bir sonraki bölümün sonunda basılıyorsa. Bastırılan dipnotlar, o bölümdeki dipnotlardan önce basılır. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Ayarlayıcı [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Ayarlayıcı [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Ayarlayıcı [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Açıklamalar


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Örnekler



Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Oluşturucunun geçerli bölümü için sayfa ayarı özelliklerini değiştirin ve metin ekleyin.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Bir belge oluşturucu kullanarak yeni bir bölüm başlatırsak,
// oluşturucunun geçerli sayfa ayarı özelliklerini devralacaktır.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Sayfa ayarı özelliklerini varsayılan değerlerine geri döndürmek için "ClearFormatting" yöntemini kullanabiliriz.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
