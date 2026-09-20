---
title: "Aspose::Words::Saving::TxtExportHeadersFootersMode 枚举"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtExportHeadersFootersMode 枚举。指定在 C++ 中页眉和页脚导出到纯文本格式的方式。"
type: docs
weight: 86000
url: /zh/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


指定页眉和页脚导出为纯文本格式的方式。

```cpp
enum class TxtExportHeadersFootersMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 不导出页眉和页脚。 |
| PrimaryOnly | 1 | 仅在每个节的开头和结尾导出主页眉和页脚。 |
| AllAtEnd | 2 | 所有页眉和页脚都放置在所有节主体之后，位于文档的最末尾。 |


## 示例



展示如何指定将页眉和页脚导出为纯文本格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 将偶数页和主页眉/页脚插入文档。
// 主页眉/页脚将覆盖偶数页的页眉/页脚。
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// 插入页面以显示这些页眉和页脚。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// 创建一个 "TxtSaveOptions" 对象，可将其传递给文档的 "Save" 方法
// 以修改我们保存文档为纯文本的方式。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// 将 "ExportHeadersFootersMode" 属性设置为 "TxtExportHeadersFootersMode.None"
// 以不导出任何页眉/页脚。
// 将 "ExportHeadersFootersMode" 属性设置为 "TxtExportHeadersFootersMode.PrimaryOnly"
// 仅导出主页眉/页脚。
// 将 "ExportHeadersFootersMode" 属性设置为 "TxtExportHeadersFootersMode.AllAtEnd"
// 将所有节主体的页眉和页脚放置在文档的末尾。
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt");

System::String newLine = System::Environment::get_NewLine();
switch (txtExportHeadersFootersMode)
{
    case Aspose::Words::Saving::TxtExportHeadersFootersMode::AllAtEnd:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Even header{0}{1}", newLine, newLine) + System::String::Format(u"Primary header{0}{1}", newLine, newLine) + System::String::Format(u"Even footer{0}{1}", newLine, newLine) + System::String::Format(u"Primary footer{0}{1}", newLine, newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::PrimaryOnly:
        ASSERT_EQ(System::String::Format(u"Primary header{0}", newLine) + System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Primary footer{0}", newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::None:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine), docText);
        break;

}
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
