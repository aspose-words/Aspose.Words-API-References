---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions 构造函数"
linktitle: "ChmLoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions 构造函数。在 C++ 中使用默认值初始化此类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


使用默认值初始化此类的新实例。

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


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
