---
title: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName 方法"
linktitle: "get_OriginalFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName 方法。CHM 文件的名称。在 C++ 中默认值为 null。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


CHM 文件的名称。默认值为 **null**。

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## 备注


CHM 文档可能包含按文件名引用同一文档的链接。Aspose.Words 支持此类链接，通常使用 [OriginalFileName](../../../aspose.words/document/get_originalfilename/) 来检查链接引用的文件是否为正在加载的文件。如果文档是从流中加载的，则应通过此属性显式指定其原始文件名，因为无法自动确定。

如果 CHM 文档是从文件加载的，并且为此属性指定了非 null 值，则该值将优先于存储在 [OriginalFileName](../../../aspose.words/document/get_originalfilename/) 中的实际文件名。

## 示例



展示如何解析类似 "ms-its:myfile.chm::/index.htm" 的 URL。
```cpp
// 我们的文档包含类似 "ms-its:amhelp.chm::....htm" 的 URL，但它有不同的名称，
// 将其保存为 HTML 后，so 文件链接无法工作。
// 我们需要在 'ChmLoadOptions' 中定义原始文件名，以避免此行为。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## 另见

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
