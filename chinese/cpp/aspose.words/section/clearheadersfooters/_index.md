---
title: "Aspose::Words::Section::ClearHeadersFooters 方法"
linktitle: "ClearHeadersFooters"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section::ClearHeadersFooters 方法。清除此节在 C++ 中的页眉和页脚。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


清除该节的页眉和页脚。

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## 备注


所有页眉和页脚的文本被清除，但 [HeaderFooter](../../headerfooter/) 对象本身未被删除。

这会使此节的页眉和页脚链接到前一节的页眉和页脚。

## 示例



展示如何清除节中所有页眉和页脚的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// 清空此节中所有页眉和页脚的所有内容。
// 页眉和页脚本身仍然存在，但将没有任何内容可显示。
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## 另见

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


清除该节的页眉和页脚。

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| preserveWatermarks | bool | 如果不应删除水印，则为 True。 |
## 备注


所有页眉和页脚的文本被清除，但 [HeaderFooter](../../headerfooter/) 对象本身未被删除。

这会使此节的页眉和页脚链接到前一节的页眉和页脚。

## 示例



展示如何在有或没有水印的情况下清除页眉和页脚的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// 添加纯文本水印。
doc->get_Watermark()->SetText(u"Aspose Watermark");

// 确保页眉和页脚有内容。
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// 删除所有页眉和页脚内容，但保留水印。
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// 删除所有页眉和页脚内容，包括水印。
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## 另见

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
