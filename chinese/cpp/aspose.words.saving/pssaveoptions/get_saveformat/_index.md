---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat 方法"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat 方法。指定在使用此保存选项对象时文档将被保存的格式。仅在 C++ 中可以是 Ps。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


指定在使用此保存选项对象时文档将被保存的格式。只能是 [Ps](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


## 示例



展示如何将文档保存为 Postscript 格式的折页形式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// 创建一个 \"PsSaveOptions\" 对象，以便我们可以将其传递给文档的 \"Save\" 方法
// 以修改该方法将文档转换为 PostScript 的方式。
// 将 \"UseBookFoldPrintingSettings\" 属性设置为 \"true\" 以排列内容
// 在输出的 Postscript 文档中，以帮助我们将其制成小册子的方式。
// 将 \"UseBookFoldPrintingSettings\" 属性设置为 \"false\" 以正常保存文档。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// 如果我们将文档渲染为小册子，则必须设置 \"MultiplePages\"
// 所有章节的页面设置对象的属性为 \"MultiplePagesType.BookFoldPrinting\"。
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// 一旦我们在页面的两面打印此文档，就可以一次性将所有页面沿中线折叠，
// 并且内容会对齐，从而形成小册子。
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
