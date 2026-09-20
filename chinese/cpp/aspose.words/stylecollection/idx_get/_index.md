---
title: "Aspose::Words::StyleCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::idx_get 方法。获取 C++ 中通过其与语言区域无关的标识符的内置样式。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


通过其与区域无关的标识符获取内置样式。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | 一个指定要检索的内置样式的 [StyleIdentifier](../../styleidentifier/) 值。 |
## 备注


当访问尚不存在的样式时，会自动创建它。

## 示例



展示如何向文档的样式集合添加一个 [Style](../../style/)。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// 为我们以后可能添加到此集合的新样式设置默认参数。
styles->get_DefaultFont()->set_Name(u"Courier New");
// 如果我们添加一个 \"StyleType.Paragraph\" 类型的样式，集合将应用这些值。
// 其 \"DefaultParagraphFormat\" 属性到样式的 \"ParagraphFormat\" 属性。
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// 添加一个样式，然后验证它具有默认设置。
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## 另见

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


按名称或别名获取样式。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## 备注


区分大小写，如果未找到具有给定名称的样式，则返回 **null**。

如果这是尚不存在的内置样式的英文名称，会自动创建它。

## 示例



显示何时重新计算文档的页面布局。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 首次将文档保存为 PDF、图像或打印时，将自动
// 缓存文档在各页中的布局。
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// 在当前版本的 Aspose.Words 中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望缓存的布局
// 保持最新，需要手动更新。
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## 另见

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


按索引获取样式。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## 示例



展示如何向文档的样式集合添加一个 [Style](../../style/)。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// 为我们以后可能添加到此集合的新样式设置默认参数。
styles->get_DefaultFont()->set_Name(u"Courier New");
// 如果我们添加一个 \"StyleType.Paragraph\" 类型的样式，集合将应用这些值。
// 其 \"DefaultParagraphFormat\" 属性到样式的 \"ParagraphFormat\" 属性。
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// 添加一个样式，然后验证它具有默认设置。
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## 另见

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
