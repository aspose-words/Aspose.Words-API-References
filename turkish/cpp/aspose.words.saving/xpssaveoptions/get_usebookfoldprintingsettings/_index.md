---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings metodu"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings metodu. C++'da MultiplePages aracılığıyla belirtilmişse, belgenin bir kitapçık baskı düzeniyle kaydedilip kaydedilmeyeceğini gösteren bir boolean değerini alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Belgenin bir kitapçık baskı düzeniyle kaydedilip kaydedilmeyeceğini gösteren bir boolean değerini alır veya ayarlar, eğer [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/) aracılığıyla belirtilmişse.

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Açıklamalar


Bu seçenek belirtilirse, kaydetme sırasında [PageSet](../../fixedpagesaveoptions/get_pageset/) yok sayılır. Bu davranış MS Word ile eşleşir. Sayfa ayarlarında kitap katlama baskı ayarları belirtilmemişse, bu seçenek hiçbir etki yapmaz.

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

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
