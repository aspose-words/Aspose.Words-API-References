---
title: "метод Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel. Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — Normal в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


## Примеры



Показывает, как указать уровень сжатия, используемый при сохранении документа OOXML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Когда мы сохраняем документ в формат OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передать его методу сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство "CompressionLevel" в "CompressionLevel.Maximum", чтобы применить самое сильное и медленное сжатие.
// Установите свойство "CompressionLevel" в "CompressionLevel.Normal", чтобы применить
// сжатие по умолчанию, которое Aspose.Words использует при сохранении документов OOXML.
// Установите свойство "CompressionLevel" в "CompressionLevel.Fast", чтобы применить более быстрое и более слабое сжатие.
// Установите свойство "CompressionLevel" в "CompressionLevel.SuperFast", чтобы применить
// сжатие по умолчанию, которое использует Microsoft Word.
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

## См. также

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
