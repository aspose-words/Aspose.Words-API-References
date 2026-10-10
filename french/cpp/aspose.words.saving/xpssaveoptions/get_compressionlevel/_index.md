---
title: "Méthode Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel. Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut est Normal en C++."
type: docs
weight: 2250
url: /fr/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut est [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Exemples



Montre comment contrôler le niveau de compression lors de l'enregistrement d'un document au format XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Créez un objet XpsSaveOptions et définissez le niveau de compression.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Voir aussi

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
