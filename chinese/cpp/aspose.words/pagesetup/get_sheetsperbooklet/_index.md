---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet 方法"
linktitle: "get_SheetsPerBooklet"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet 方法。返回或设置每个小册子中包含的页面数量（C++）。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


返回或设置每本小册子包含的页数。

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
