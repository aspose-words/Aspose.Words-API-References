---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel 方法"
linktitle: "get_NavigationMapLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel 方法。指定在导出到 EPUB、MOBI 或 AZW3 格式时，导航映射中填充的标题的最大级别。默认值在 C++ 中为 %3。"
type: docs
weight: 40500
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


指定在导出为 EPUB、MOBI 或 AZW3 格式时填充到导航地图的标题最大层级。默认值为 **%3**。

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## 备注


导航映射允许用户代理提供一种便捷的方式在文档结构中进行导航。通常导航点对应文档中的标题。要填充至 **N** 级别的标题，请将此值分配给 [NavigationMapLevel](./)。

默认情况下，会填充三级标题：样式为 **Heading 1**、**Heading 2** 和 **Heading 3** 的段落。您可以将此属性设置为 1 到 9 之间的值，以请求相应的最大级别。将其设为零将把导航映射仅缩减为文档根或文档部分的根。

## 示例



展示如何为 Azw3 文档生成目录。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


展示如何为 Mobi 文档生成目录。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
