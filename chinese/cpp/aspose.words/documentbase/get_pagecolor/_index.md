---
title: "Aspose::Words::DocumentBase::get_PageColor 方法"
linktitle: "get_PageColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::get_PageColor 方法。获取或设置文档的页面颜色。此属性是 C++ 中 BackgroundShape 的简化版本。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


获取或设置文档的页面颜色。此属性是 [BackgroundShape](../get_backgroundshape/) 的简化版本。

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## 备注


此属性提供了一种简便的方法来为文档指定纯色页面颜色。设置此属性会创建并设置适当的 [BackgroundShape](../get_backgroundshape/)。

如果未设置页面颜色（例如文档中没有背景形状），则返回 **Empty**。

## 示例



展示如何为文档的所有页面设置背景颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## 另见

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
