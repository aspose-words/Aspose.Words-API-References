---
title: "Aspose::Words::Settings::MultiplePagesType 枚举"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::MultiplePagesType 枚举。指定文档在 C++ 中的打印方式。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


指定文档的打印方式。

```cpp
enum class MultiplePagesType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 普通 | 0 | 普通打印，未指定多页。 |
| MirrorMargins | 1 | 在相对页上交换左右页边距。 |
| TwoPagesPerSheet | 2 | 每张纸打印两页。 |
| BookFoldPrinting | 3 | 指定是否将文档打印为书折形式。 |
| BookFoldPrintingReverse | 4 | 指定是否将文档打印为反向书折形式。 |
| Default | n/a | 默认值是 [Normal](./) |


## 示例



展示如何配置可以打印为书折的文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入跨越 16 页的文本。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// 配置第一节的 \"PageSetup\" 属性，以书折形式打印文档。
// 当我们双面打印此文档时，可以将页面取出堆叠它们
// 并一次性沿中线全部折叠。文档的内容将对齐成书折。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// 我们只能以 4 的倍数指定纸张数量。
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
