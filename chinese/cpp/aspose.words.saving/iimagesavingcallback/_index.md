---
title: "Aspose::Words::Saving::IImageSavingCallback interface"
linktitle: "IImageSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IImageSavingCallback 接口。如果您想控制 Aspose.Words 在将文档保存为 HTML 时如何保存图像，请实现此接口。可在 C++ 中用于其他格式。"
type: docs
weight: 43000
url: /zh/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


如果您想控制 Aspose.Words 在将文档保存为 HTML 时如何保存图像，请实现此接口。也可用于其他格式。

```cpp
class IImageSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | 当 Aspose.Words 将图像保存为 HTML 时调用。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
