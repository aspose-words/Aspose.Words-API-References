---
title: "Aspose::Words::Saving::Zip64Mode Enum"
linktitle: "Zip64Mode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::Zip64Mode Enum. Gibt an, wann ZIP64-Format-Erweiterungen für OOXML-Dateien in C++ verwendet werden sollen."
type: docs
weight: 88000
url: /de/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


Gibt an, wann ZIP64-Formatserweiterungen für OOXML-Dateien verwendet werden sollen.

```cpp
enum class Zip64Mode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Niemals | 0 | Verwenden Sie keine ZIP64-Format-Erweiterungen. |
| IfNecessary | 1 | Falls erforderlich, ZIP64-Format-Erweiterungen verwenden. |
| Immer | 2 | Immer ZIP64-Format-Erweiterungen verwenden. |


## Beispiele



Zeigt, wie ZIP64-Format-Erweiterungen verwendet werden.
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
