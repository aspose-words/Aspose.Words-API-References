---
title: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer 方法"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer 方法。获取或设置一个值，以确定在 C++ 中保存为 EMF 时是使用 GDI+ 还是 Aspose.Words 元文件渲染器。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


获取或设置生成图像的垂直分辨率（单位为每英寸点数）。

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## 备注


如果设置为 **true**，则使用 GDI+ 元文件渲染器。即内容写入 GDI+ 图形对象并保存为元文件。

如果设置为 **false**，则使用 Aspose.Words 元文件渲染器。即内容直接使用 Aspose.Words 写入元文件格式。

仅在保存为 EMF 时生效。

GDI+ 保存仅在 .NET 上工作。

默认值为 **true**。

## 示例



展示了在将文档转换为 .emf 时如何选择渲染器。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 当我们将文档保存为 EMF 图像时，可以传递一个 SaveOptions 对象来为图像选择渲染器。
// 如果我们将 "UseGdiEmfRenderer" 标志设置为 "true"，Aspose.Words 将使用 GDI+ 渲染器。
// 如果我们将 "UseGdiEmfRenderer" 标志设置为 "false"，Aspose.Words 将使用其自己的元文件渲染器。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## 另见

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
