---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings yöntemi"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings yöntemi. Belgenin MultiplePages aracılığıyla belirtildiği takdirde bir kitapçık baskı düzeni kullanılarak kaydedilip kaydedilmeyeceğini gösteren boolean bir değeri alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


Belgenin bir kitapçık baskı düzeniyle kaydedilip kaydedilmeyeceğini gösteren bir boolean değerini alır veya ayarlar, eğer [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/) aracılığıyla belirtilmişse.

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Açıklamalar


Bu seçenek belirtilirse, kaydetme sırasında [PageSet](../../fixedpagesaveoptions/get_pageset/) yok sayılır. Bu davranış MS Word ile eşleşir. Sayfa ayarlarında kitap katlama baskı ayarları belirtilmemişse, bu seçenek hiçbir etki yapmaz.

## Örnekler



Bir belgeyi kitap katlaması şeklinde Postscript formatına kaydetmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// "PsSaveOptions" nesnesi oluşturup belgeye ait "Save" yöntemine geçirebiliriz
// bu yöntemin belgeyi PostScript'e nasıl dönüştürdüğünü değiştirmek için.
// "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın, içerikleri düzenlemek için
// çıktı Postscript belgesinde bir kitapçık oluşturmayı kolaylaştıracak şekilde.
// "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayarak belgeyi normal şekilde kaydedin.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Belgeyi bir kitapçık olarak işliyorsak, "MultiplePages" özelliğini ayarlamalıyız
// tüm bölümlerin sayfa ayarı nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak.
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Bu belgeyi sayfaların her iki tarafına bastıktan sonra, tüm sayfaları bir anda ortasından katlayabiliriz,
// ve içerikler bir kitapçık oluşturacak şekilde hizalanır.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## Ayrıca Bakınız

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
