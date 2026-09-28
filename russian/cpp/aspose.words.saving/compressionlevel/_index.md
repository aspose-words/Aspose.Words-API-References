---
title: "Aspose::Words::Saving::CompressionLevel enum"
linktitle: "CompressionLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::CompressionLevel enum. Уровень сжатия для файлов OOXML и XPS. (Файлы DOCX, DOTX и XPS внутренне являются ZIP-архивом, это свойство управляет уровнем сжатия архива. Обратите внимание, что файл FlatOpc не является ZIP-архивом, поэтому это свойство не влияет на файлы FlatOpc.) в C++."
type: docs
weight: 47000
url: /ru/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Уровень сжатия для файлов OOXML и XPS. (Файлы DOCX, DOTX и XPS внутренне являются ZIP-архивом, это свойство управляет уровнем сжатия архива. Обратите внимание, что файл FlatOpc не является ZIP-архивом, поэтому это свойство не влияет на файлы FlatOpc.)

```cpp
enum class CompressionLevel
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Normal | 0 | Обычный уровень сжатия. Уровень сжатия по умолчанию, используемый [Aspose.Words](../../aspose.words/). |
| Maximum | 1 | Максимальный уровень сжатия. |
| Fast | 2 | Быстрый уровень сжатия. |
| SuperFast | 3 | Уровень сжатия Super Fast. Microsoft Word использует этот уровень сжатия. |


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


Показывает, как управлять уровнем сжатия при сохранении документа в формат XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Создайте объект XpsSaveOptions и задайте уровень сжатия.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
