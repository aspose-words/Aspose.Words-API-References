---
title: "Aspose::Words::PageExtractOptions 类"
linktitle: "PageExtractOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageExtractOptions 类。允许在 C++ 中指定文档页面提取的选项。"
type: docs
weight: 45500
url: /zh/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


允许指定文档页面提取的选项。

```cpp
class PageExtractOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | 指定结果文档中的 NUMPAGES 字段是否会被其实际结果值替换。默认值为 **true**。 |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | 指定结果文档中的起始页码是否应更新。默认值为 **true**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | 用于设置 [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)。 |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | 用于设置 [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何重置初始页码并保存 NUMPAGE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// 默认行为：
// 提取的页码与原始文档中的相同，就好像我们在 MS Word 中选择了"Print 2 pages"。
// 起始页将被设置为 2，指示页数的字段将被移除
// 并替换为等于页数的常量值。
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// 更改后的行为：
// 提取的页码已重置，并开始新的页码，
// 好像我们已经复制了第二页的内容并粘贴到一个新文档中。
// 起始页将设置为 1，指示页数的字段将保持不变
// 并将显示当前的页数。
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
