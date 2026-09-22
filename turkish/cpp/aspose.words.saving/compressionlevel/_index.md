---
title: "Aspose::Words::Saving::CompressionLevel enum"
linktitle: "CompressionLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::CompressionLevel enum. OOXML ve XPS dosyaları için sıkıştırma seviyesi. (DOCX, DOTX ve XPS dosyaları dahili olarak bir ZIP arşivi olup, bu özellik arşivin sıkıştırma seviyesini kontrol eder. FlatOpc dosyasının bir ZIP arşivi olmadığını unutmayın, bu nedenle bu özellik FlatOpc dosyalarını etkilemez.) C++'ta."
type: docs
weight: 47000
url: /tr/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


OOXML ve XPS dosyaları için sıkıştırma seviyesi. (DOCX, DOTX ve XPS dosyaları dahili olarak bir ZIP arşivi olup, bu özellik arşivin sıkıştırma seviyesini kontrol eder. FlatOpc dosyasının ZIP arşivi olmadığını unutmayın, bu nedenle bu özellik FlatOpc dosyalarını etkilemez.)

```cpp
enum class CompressionLevel
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Normal | 0 | Normal sıkıştırma seviyesi. [Aspose.Words](../../aspose.words/) tarafından kullanılan varsayılan sıkıştırma seviyesi. |
| Maximum | 1 | Maksimum sıkıştırma seviyesi. |
| Fast | 2 | Hızlı sıkıştırma seviyesi. |
| SuperFast | 3 | Süper hızlı sıkıştırma seviyesi. Microsoft Word bu sıkıştırma seviyesini kullanır. |


## Örnekler



OOXML belgesi kaydederken kullanılacak sıkıştırma seviyesinin nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Belgeyi OOXML formatında kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgeyi kaydetme yöntemine geçirerek belgeyi nasıl kaydedeceğimizi değiştirebiliriz.
// En güçlü ve en yavaş sıkıştırmayı uygulamak için "CompressionLevel" özelliğini "CompressionLevel.Maximum" olarak ayarlayın.
// Uygulamak için "CompressionLevel" özelliğini "CompressionLevel.Normal" olarak ayarlayın
// Aspose.Words'un OOXML belgeleri kaydederken kullandığı varsayılan sıkıştırma.
// Daha hızlı ve daha zayıf bir sıkıştırma uygulamak için "CompressionLevel" özelliğini "CompressionLevel.Fast" olarak ayarlayın.
// Uygulamak için "CompressionLevel" özelliğini "CompressionLevel.SuperFast" olarak ayarlayın
// Microsoft Word'un kullandığı varsayılan sıkıştırma.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_CompressionLevel(compressionLevel);

System::SharedPtr<System::Diagnostics::Stopwatch> st = System::Diagnostics::Stopwatch::StartNew();
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st->Stop();

auto fileInfo = System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx");

std::cout << System::String::Format(u"Saving operation done using the \"{0}\" compression level:", compressionLevel) << std::endl;
std::cout << System::String::Format(u"\tDuration:\t{0} ms", st->get_ElapsedMilliseconds()) << std::endl;
std::cout << System::String::Format(u"\tFile Size:\t{0} bytes", fileInfo->get_Length()) << std::endl;
```


Bir belgeyi XPS formatında kaydederken sıkıştırma seviyesini nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Bir XpsSaveOptions nesnesi oluşturun ve sıkıştırma seviyesini ayarlayın.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
