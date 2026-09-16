---
title: "Aspose::Words::Loading::BlockImportMode 枚举"
linktitle: "BlockImportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::BlockImportMode 枚举。指定如何从基于 HTML 的文档中导入块级元素的属性（在 C++ 中）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


指定块级元素的属性如何从基于 HTML 的文档中导入。

```cpp
enum class BlockImportMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Merge | 0 | 父块的[属性](../../aspose.words.properties/)被合并并存储在子元素上（即段落或表格）。 |
| Preserve | 1 | 父块的[属性](../../aspose.words.properties/)被导入到一个特殊的逻辑结构中，并且与文档节点分开存储。 |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
