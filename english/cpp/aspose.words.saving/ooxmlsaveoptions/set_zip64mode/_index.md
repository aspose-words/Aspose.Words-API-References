---
title: Aspose::Words::Saving::OoxmlSaveOptions::set_Zip64Mode method
linktitle: set_Zip64Mode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OoxmlSaveOptions::set_Zip64Mode method. Specifies whether or not to use ZIP64 format extensions for the output document. The default value is Never in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.saving/ooxmlsaveoptions/set_zip64mode/
---
## OoxmlSaveOptions::set_Zip64Mode method


Specifies whether or not to use ZIP64 format extensions for the output document. The default value is [Never](../../zip64mode/).

```cpp
void Aspose::Words::Saving::OoxmlSaveOptions::set_Zip64Mode(Aspose::Words::Saving::Zip64Mode value)
```

## Examples


Shows how to use ZIP64 format extensions.

```cpp
auto random = System::MakeObject<System::Random>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

for (int32_t i = 0; i < 10000; i++)
{
    {
        auto bmp = System::MakeObject<System::Drawing::Bitmap>(5, 5);
        {
            System::SharedPtr<System::Drawing::Graphics> g = System::Drawing::Graphics::FromImage(bmp);
            g->Clear(System::Drawing::Color::FromArgb(random->Next(0, 254), random->Next(0, 254), random->Next(0, 254)));
            {
                auto ms = System::MakeObject<System::IO::MemoryStream>();
                bmp->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
                builder->InsertImage(ms->ToArray());
            }
        }
    }
}
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Zip64Mode(Zip64Mode::Always);

builder->get_Document()->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
```
## See Also

* [Zip64Mode](../get_zip64mode/)

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
