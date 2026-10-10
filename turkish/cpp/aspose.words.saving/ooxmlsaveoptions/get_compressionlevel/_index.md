---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel yöntemi"
linktitle: "get_CompressionLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel yöntemi. Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer C++'da Normal'dir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer [Normal](../../compressionlevel/) dir.

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


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

## Ayrıca Bakınız

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
