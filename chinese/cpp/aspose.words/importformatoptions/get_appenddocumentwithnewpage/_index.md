---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage 方法"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage 方法。获取或设置一个布尔值，指示在调用 AppendDocument() 时是否强制将第一个导入的节类型更改为 NewPage。默认值在 C++ 中为 true。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


获取或设置一个布尔值，指示在调用 [AppendDocument()](../) 时是否强制将第一个导入的节类型更改为 [NewPage](../../sectionstart/)。默认值为 **true**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## 示例



展示如何保留原始节类型。
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
