---
title: "énumération Aspose::Words::Saving::Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "énumération Aspose::Words::Saving::Zip64Mode. Spécifie quand utiliser les extensions de format ZIP64 pour les fichiers OOXML en C++."
type: docs
weight: 88000
url: /fr/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


Spécifie quand utiliser les extensions du format ZIP64 pour les fichiers OOXML.

```cpp
enum class Zip64Mode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Jamais | 0 | Ne pas utiliser les extensions de format ZIP64. |
| IfNecessary | 1 | Si nécessaire, utilisez les extensions de format ZIP64. |
| Toujours | 2 | Toujours utiliser les extensions de format ZIP64. |


## Exemples



Montre comment utiliser les extensions de format ZIP64.
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

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
