---
title: Aspose::Words::Saving::Zip64Mode enum
linktitle: Zip64Mode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::Zip64Mode enum. Specifies when to use ZIP64 format extensions for OOXML files in C++.'
type: docs
weight: 88000
url: /cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


Specifies when to use ZIP64 format extensions for OOXML files.

```cpp
enum class Zip64Mode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Never | 0 | Do not use ZIP64 format extensions. |
| IfNecessary | 1 | If necessary use ZIP64 format extensions. |
| Always | 2 | Always use ZIP64 format extensions. |


## Examples



Shows how to use ZIP64 format extensions. 
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

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
