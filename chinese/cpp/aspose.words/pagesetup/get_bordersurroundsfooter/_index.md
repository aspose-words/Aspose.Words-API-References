---
title: "Aspose::Words::PageSetup::get_BorderSurroundsFooter 方法"
linktitle: "get_BorderSurroundsFooter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_BorderSurroundsFooter 方法。指定页面边框在 C++ 中是否包括或排除页脚。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/pagesetup/get_bordersurroundsfooter/
---
## PageSetup::get_BorderSurroundsFooter method


指定页面边框是否包括或排除页脚。

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsFooter()
```


## 示例



展示如何将边框应用于页面和页眉/页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// 插入蓝色双线边框。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// 节的 PageSetup 对象具有 "BorderSurroundsHeader" 和 "BorderSurroundsFooter" 标志，用于确定
// 页面边框是否环绕正文文本，同时分别包括页眉或页脚。
// 将 "BorderSurroundsHeader" 标志设置为 "true" 以用我们的边框环绕页眉，
// 然后将 "BorderSurroundsFooter" 标志设置为，使页脚位于边框之外。
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
