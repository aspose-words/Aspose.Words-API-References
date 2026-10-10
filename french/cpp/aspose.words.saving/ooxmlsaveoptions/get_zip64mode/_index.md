---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Zip64Mode méthode"
linktitle: "get_Zip64Mode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Zip64Mode méthode. Spécifie s'il faut ou non utiliser les extensions de format ZIP64 pour le document de sortie. La valeur par défaut est Never en C++."
type: docs
weight: 7500
url: /fr/cpp/aspose.words.saving/ooxmlsaveoptions/get_zip64mode/
---
## OoxmlSaveOptions::get_Zip64Mode method


Spécifie s'il faut ou non utiliser les extensions de format ZIP64 pour le document de sortie. La valeur par défaut est [Never](../../zip64mode/).

```cpp
Aspose::Words::Saving::Zip64Mode Aspose::Words::Saving::OoxmlSaveOptions::get_Zip64Mode() const
```


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

* Enum [Zip64Mode](../../zip64mode/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
