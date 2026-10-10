---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat yöntemi"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. C++'de yalnızca Ps olabilir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Ps](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
