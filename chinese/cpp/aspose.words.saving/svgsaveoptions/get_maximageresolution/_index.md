---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution 方法"
linktitle: "get_MaxImageResolution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution 方法。获取或设置以每英寸像素为单位的值，用于限制导出光栅图像的分辨率。默认值在 C++ 中为零。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


获取或设置以每英寸像素为单位的值，用于限制导出栅格图像的分辨率。默认值为零。

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## 备注


如果此属性的值非零，则会限制导出光栅图像的分辨率。也就是说，分辨率较高的图像会被重新采样至该限制，而分辨率较低的图像则保持原样导出。

如果此属性的值为零，所有光栅图像将在不进行重新采样的情况下导出。

## 示例



展示如何设置图像分辨率的限制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## 另见

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
