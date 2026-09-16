---
title: "Aspose::Words::HtmlInsertOptions 枚举"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::HtmlInsertOptions 枚举。指定 C++ 中 InsertHtml() 方法的选项。"
type: docs
weight: 92000
url: /zh/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


指定 [InsertHtml()](../) 方法的选项。

```cpp
enum class HtmlInsertOptions
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 插入 HTML 时使用默认选项。 |
| UseBuilderFormatting | 1 | 使用在 [DocumentBuilder](../documentbuilder/) 中指定的字体和段落格式作为从 HTML 插入的文本的基础格式。 |
| RemoveLastEmptyParagraph | 2 | 移除在以块级元素结束的 HTML 后通常插入的空段落。 |
| PreserveBlocks | 4 | 保留块级元素的属性。 |


## 示例



展示如何更好地保留可见的边框和外边距。
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// 设置导入 HTML 块级元素的新模式。
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
