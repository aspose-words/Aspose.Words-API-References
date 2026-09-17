---
title: "Méthode Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet"
linktitle: "get_PageSet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet. Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Exemples



Montre comment extraire des pages en fonction d'indices de page exacts.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez cinq pages au document.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Créez un objet "XpsSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Utilisez la propriété "PageSet" pour sélectionner un ensemble de pages du document à enregistrer dans le XPS de sortie.
// Dans ce cas, nous choisirons, via un indice zéro basé, seulement trois pages : page 1, page 2 et page 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Voir aussi

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
