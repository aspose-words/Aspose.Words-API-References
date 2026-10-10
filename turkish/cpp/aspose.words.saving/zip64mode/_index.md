---
title: "Aspose::Words::Saving::Zip64Mode enum"
linktitle: "Zip64Mode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::Zip64Mode enum. C++'da OOXML dosyaları için ZIP64 format uzantılarının ne zaman kullanılacağını belirtir."
type: docs
weight: 88000
url: /tr/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


OOXML dosyaları için ZIP64 format uzantılarının ne zaman kullanılacağını belirtir.

```cpp
enum class Zip64Mode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Asla | 0 | ZIP64 format uzantılarını kullanma. |
| Gerekirse | 1 | Gerekirse ZIP64 format uzantılarını kullan. |
| Her zaman | 2 | Her zaman ZIP64 format uzantılarını kullan. |


## Örnekler



ZIP64 format uzantılarını nasıl kullanacağınızı gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
