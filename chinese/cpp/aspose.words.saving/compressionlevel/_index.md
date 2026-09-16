---
title: "Aspose::Words::Saving::CompressionLevel 枚举"
linktitle: "CompressionLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::CompressionLevel 枚举。用于 OOXML 和 XPS 文件的压缩级别。（DOCX、DOTX 和 XPS 文件在内部是 ZIP 压缩包，此属性控制压缩包的压缩级别。请注意，FlatOpc 文件不是 ZIP 压缩包，因此此属性不影响 FlatOpc 文件。）在 C++ 中。"
type: docs
weight: 47000
url: /zh/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


OOXML 和 XPS 文件的压缩级别。（DOCX、DOTX 和 XPS 文件内部是 ZIP 压缩包，此属性控制压缩包的压缩级别。注意，FlatOpc 文件不是 ZIP 压缩包，因此此属性不影响 FlatOpc 文件。）

```cpp
enum class CompressionLevel
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Normal | 0 | 普通压缩级别。由 [Aspose.Words](../../aspose.words/) 使用的默认压缩级别。 |
| Maximum | 1 | 最大压缩级别。 |
| 快速 | 2 | 快速压缩级别。 |
| 超快速 | 3 | 超快速压缩级别。Microsoft Word 使用此压缩级别。 |


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


展示如何在将文档保存为 XPS 格式时控制压缩级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// 创建一个 XpsSaveOptions 对象并设置压缩级别。
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
