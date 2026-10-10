---
title: "Aspose::Words::Saving::Zip64Mode enum"
linktitle: "Zip64Mode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::Zip64Mode enum. Specifica quando utilizzare le estensioni del formato ZIP64 per i file OOXML in C++."
type: docs
weight: 88000
url: /it/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


Specifica quando utilizzare le estensioni del formato ZIP64 per i file OOXML.

```cpp
enum class Zip64Mode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Mai | 0 | Non utilizzare le estensioni del formato ZIP64. |
| IfNecessary | 1 | Se necessario, utilizza le estensioni del formato ZIP64. |
| Sempre | 2 | Utilizza sempre le estensioni del formato ZIP64. |


## Esempi



Mostra come utilizzare le estensioni del formato ZIP64.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
