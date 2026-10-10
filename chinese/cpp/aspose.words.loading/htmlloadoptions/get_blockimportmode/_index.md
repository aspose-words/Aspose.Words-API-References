---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode 方法"
linktitle: "get_BlockImportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode 方法。获取或设置一个值，以指定块级元素的属性如何导入。默认值在 C++ 中为 Merge。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


获取或设置一个值，以指定块级元素的属性如何导入。默认值为 [Merge](../../blockimportmode/)。

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


## 示例



展示块级元素的属性如何从基于 HTML 的文档中导入。
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// 设置导入 HTML 块级元素的新模式。
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## 另见

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
