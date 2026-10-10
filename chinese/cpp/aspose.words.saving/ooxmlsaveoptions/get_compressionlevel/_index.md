---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel 方法"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel 方法。指定用于保存文档的压缩级别。默认值为 Normal（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


指定用于保存文档的压缩级别。默认值为 [Normal](../../compressionlevel/)。

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


## 示例



展示如何在保存 OOXML 文档时指定使用的压缩级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// 当我们将文档保存为 OOXML 格式时，可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法，以修改文档的保存方式。
// 将 "CompressionLevel" 属性设置为 "CompressionLevel.Maximum" 以应用最强且最慢的压缩。
// 将 "CompressionLevel" 属性设置为 "CompressionLevel.Normal" 以应用
// Aspose.Words 在保存 OOXML 文档时使用的默认压缩。
// 将 "CompressionLevel" 属性设置为 "CompressionLevel.Fast" 以应用更快且更弱的压缩。
// 将 "CompressionLevel" 属性设置为 "CompressionLevel.SuperFast" 以应用
// Microsoft Word 使用的默认压缩。
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

## 另见

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
