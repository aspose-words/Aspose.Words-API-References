---
title: "Aspose::Words::Saving::Zip64Mode enum"
linktitle: "Zip64Mode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::Zip64Mode enum. Указывает, когда использовать расширения формата ZIP64 для файлов OOXML в C++."
type: docs
weight: 88000
url: /ru/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


Указывает, когда использовать расширения формата ZIP64 для файлов OOXML.

```cpp
enum class Zip64Mode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Никогда | 0 | Не использовать расширения формата ZIP64. |
| IfNecessary | 1 | При необходимости использовать расширения формата ZIP64. |
| Всегда | 2 | Всегда использовать расширения формата ZIP64. |


## Примеры



Показывает, как использовать расширения формата ZIP64.
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

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
