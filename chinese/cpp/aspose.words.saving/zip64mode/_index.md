---
title: "Aspose::Words::Saving::Zip64Mode 枚举"
linktitle: "Zip64Mode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::Zip64Mode 枚举。指定在 C++ 中何时对 OOXML 文件使用 ZIP64 格式扩展。"
type: docs
weight: 88000
url: /zh/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


指定何时在 OOXML 文件中使用 ZIP64 格式扩展。

```cpp
enum class Zip64Mode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 从不 | 0 | 不要使用 ZIP64 格式扩展。 |
| IfNecessary | 1 | 如有必要，使用 ZIP64 格式扩展。 |
| 始终 | 2 | 始终使用 ZIP64 格式扩展。 |


## 示例



展示如何使用 ZIP64 格式扩展。
```cpp
System::Random random;
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

for (int32_t i = 0; i < 10000; i++)
{
    {
        auto bmp = System::MakeObject<System::Drawing::Bitmap>(5, 5);
        {
            System::SharedPtr<System::Drawing::Graphics> g = System::Drawing::Graphics::FromImage(bmp);
            g->Clear(System::Drawing::Color::FromArgb(random.Next(0, 254), random.Next(0, 254), random.Next(0, 254)));
            {
                auto ms = System::MakeObject<System::IO::MemoryStream>();
                bmp->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
                builder->InsertImage(ms->ToArray());
            }
        }
    }
}
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Zip64Mode(Aspose::Words::Saving::Zip64Mode::Always);

builder->get_Document()->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
