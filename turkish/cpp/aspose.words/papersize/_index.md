---
title: "Aspose::Words::PaperSize enum"
linktitle: "PaperSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PaperSize enum. C++'da kağıt boyutunu belirtir."
type: docs
weight: 109000
url: /tr/cpp/aspose.words/papersize/
---
## PaperSize enum


Kağıt boyutunu belirtir.

```cpp
enum class PaperSize
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| A3 | 0 | 297 x 420 mm. |
| A4 | 1 | 210 x 297 mm. |
| A5 | 2 | 148 x 210 mm. |
| B4 | 3 | 250 x 353 mm. |
| B5 | 4 | 176 x 250 mm. |
| Executive | 5 | 7.25 x 10.5 inç. |
| Folio | 6 | 8.5 x 13 inç. |
| Ledger | 7 | 17 x 11 inç. |
| Legal | 8 | 8.5 x 14 inç. |
| Letter | 9 | 8.5 x 11 inç. |
| EnvelopeDL | 10 | 110 x 220 mm. |
| Quarto | 11 | 8.47 x 10.83 inç. |
| Statement | 12 | 8.5 x 5.5 inç. |
| Tabloid | 13 | 11 x 17 inç. |
| Paper10x14 | 14 | 10 x 14 inç. |
| Paper11x17 | 15 | 11 x 17 inç. |
| Number10Envelope | 16 | 4.125 x 9.5 inç. |
| JisB4 | 17 | 257 x 364 mm. |
| JisB5 | 18 | 182 x 257 mm. |
| Özel | 19 | Özel kağıt boyutu. |


## Örnekler



Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Sayfa boyutlarının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Mevcut sayfanın boyutunu önceden tanımlı bir boyuta değiştirebiliriz
// "PaperSize" özelliğini bu bölümün PageSetup nesnesi aracılığıyla kullanarak.
builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Tabloid);

ASPOSE_ASSERT_EQ(792.0, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(1224.0, builder->get_PageSetup()->get_PageHeight());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

// Her bölümün kendi PageSetup nesnesi vardır. Bir belge oluşturucu kullanarak yeni bir bölüm oluşturduğumuzda,
// o bölümün PageSetup nesnesi, önceki bölümün PageSetup nesnesinin tüm değerlerini devralır.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

ASSERT_EQ(Aspose::Words::PaperSize::Tabloid, builder->get_PageSetup()->get_PaperSize());

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::A5);
builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

ASPOSE_ASSERT_EQ(419.55, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(595.30, builder->get_PageSetup()->get_PageHeight());

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

// Bu bölümün sayfaları için özel bir boyut ayarlayın.
builder->get_PageSetup()->set_PageWidth(620);
builder->get_PageSetup()->set_PageHeight(480);

ASSERT_EQ(Aspose::Words::PaperSize::Custom, builder->get_PageSetup()->get_PaperSize());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

doc->Save(get_ArtifactsDir() + u"PageSetup.PaperSizes.docx");
```


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
