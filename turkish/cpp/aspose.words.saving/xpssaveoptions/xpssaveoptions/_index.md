---
title: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions yapıcı"
linktitle: "XpsSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions yapıcı. C++'ta Xps biçiminde bir belge kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Bu sınıfın, [Xps](../../../aspose.words/saveformat/) biçiminde bir belge kaydetmek için kullanılabilecek yeni bir örneğini başlatır.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Örnekler



Kaydedilen bir XPS belgesinin taslak (outline) içinde görünecek başlık seviyelerinin nasıl sınırlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Seviye 1, 2 ve ardından 3 olan başlıkları, TOC (İçindekiler) girdileri olarak ekleyin.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// \"XpsSaveOptions\" nesnesi oluşturun; bu nesneyi belgenin \"Save\" yöntemine geçebiliriz
// bu yöntemin belgeyi .XPS'ye nasıl dönüştürdüğünü değiştirmek için.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Çıktı XPS belgesi bir taslak, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu içerecektir.
// Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürür.
// \"HeadingsOutlineLevels\" özelliğini \"2\" olarak ayarlayın; böylece seviyeleri 2'nin üzerindeki tüm başlıklar taslaktan dışlanır.
// Yukarıda eklediğimiz son iki başlık görünmeyecek.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Ayrıca Bakınız

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Bu sınıfın, [Xps](../../../aspose.words/saveformat/) veya [OpenXps](../../../aspose.words/saveformat/) biçiminde bir belge kaydetmek için kullanılabilecek yeni bir örneğini başlatır.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


## Örnekler



Bir belgeyi XPS biçiminde kitap katlaması şeklinde nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// \"XpsSaveOptions\" nesnesi oluşturun; bu nesneyi belgenin \"Save\" yöntemine geçebiliriz
// bu yöntemin belgeyi .XPS'ye nasıl dönüştürdüğünü değiştirmek için.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın, içerikleri düzenlemek için
// çıktı XPS'yi bir broşür oluşturmak için kullanmamıza yardımcı olacak şekilde.
// "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın, böylece XPS normal olarak işlenir.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Belgeyi bir kitapçık olarak işliyorsak, "MultiplePages" özelliğini ayarlamalıyız
// tüm bölümlerin sayfa ayarı nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak.
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Bu belgeyi yazdırdıktan sonra sayfaları istifleyerek bir broşüre dönüştürebiliriz.
// yazıcıdan çıkıp ortadan katlanarak.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
