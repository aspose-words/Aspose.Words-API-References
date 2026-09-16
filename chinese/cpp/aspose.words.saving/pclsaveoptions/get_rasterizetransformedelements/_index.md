---
title: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements 方法"
linktitle: "get_RasterizeTransformedElements"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements 方法。获取或设置一个值，以确定在保存为 PCL 文档之前是否应对复杂的变换元素进行栅格化。默认在 C++ 中为 true。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


获取或设置一个值，以确定在保存为 PCL 文档之前是否应对复杂的变换元素进行光栅化。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## 示例



展示在将文档保存为 PCL 时如何对复杂元素进行光栅化。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## 另见

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
