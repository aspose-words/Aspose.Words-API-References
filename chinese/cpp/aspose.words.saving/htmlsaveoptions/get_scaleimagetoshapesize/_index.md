---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize 方法"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize 方法。指定在导出为 HTML、MHTML 或 EPUB 时，是否由 Aspose.Words 将图像缩放到其所在形状的边界大小。默认值在 C++ 中为 true。"
type: docs
weight: 46000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


指定在导出为 HTML、MHTML 或 EPUB 时，图像是否由 Aspose.Words 按边界形状大小进行缩放。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## 备注


Microsoft Word 文档中的图像是一种形状。形状有尺寸，图像也有自己的尺寸。这些尺寸并非直接关联。例如，图像可以是 1024x786 像素，但显示该图像的形状可能是 400x300 点。

为了在浏览器中显示图像，必须将其缩放到形状大小。[ScaleImageToShapeSize](./) 属性控制图像缩放发生的位置：在 Aspose.Words 导出为 HTML 时进行，或在浏览器中显示文档时进行。

当 [ScaleImageToShapeSize](./) 为 **true** 时，图像在导出为 HTML 时由 [Aspose.Words](../../../aspose.words/) 使用高质量缩放进行缩放。当 [ScaleImageToShapeSize](./) 为 **false** 时，图像以原始大小输出，浏览器需要自行缩放。

一般来说，浏览器进行快速且质量较差的缩放。因此，当 [ScaleImageToShapeSize](./) 为 **true** 时，通常可以在浏览器中获得更好的显示质量和更小的文件大小；而当 [ScaleImageToShapeSize](./) 为 **false** 时，则可以获得更好的打印质量和更快的转换速度。

除了包含单个光栅图像的形状外，此选项还影响由光栅图像组成的组合形状。如果 [ScaleImageToShapeSize](./) 为 **false** 且一个组合形状包含的光栅图像其固有分辨率高于 [ImageResolution](../get_imageresolution/) 中指定的值，Aspose.Words 将提升该组合的渲染分辨率。这使得在保存为 HTML 时能够更好地保留组合高分辨率图像的质量。

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
