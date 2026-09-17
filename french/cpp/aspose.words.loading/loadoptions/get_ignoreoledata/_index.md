---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method"
linktitle: "get_IgnoreOleData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method. Indique s'il faut ignorer les données OLE en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


Spécifie s'il faut ignorer les données OLE.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Remarques


Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.

La valeur par défaut est **false**.

## Exemples



Montre comment ignorer les données OLE lors du chargement.
```cpp
// Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances
// sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
