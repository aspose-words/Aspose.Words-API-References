---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat méthode"
linktitle: "SaveFormatToLoadFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat méthode. Convertit une valeur SaveFormat en une valeur LoadFormat si possible en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Convertit une valeur [SaveFormat](../../saveformat/) en une valeur [LoadFormat](../../loadformat/) si possible.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Exemples



Montre comment convertir un format d'enregistrement en son format de chargement correspondant.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Certains types de fichiers peuvent permettre d'enregistrer des documents, mais pas de les charger avec Aspose.Words.
// Si nous essayons de convertir un format d'enregistrement de ce type en un format de chargement, une exception sera levée.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## Voir aussi

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
