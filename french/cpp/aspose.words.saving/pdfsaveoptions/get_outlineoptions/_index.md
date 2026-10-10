---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions méthode"
linktitle: "get_OutlineOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions. Permet de spécifier les options de plan dans C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_outlineoptions/
---
## PdfSaveOptions::get_OutlineOptions method


Permet de spécifier les options de contour.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions() const
```

## Remarques


Les plans peuvent être créés à partir des titres et des signets.

Pour les titres, le niveau du plan est déterminé par le niveau du titre.

Il est possible de définir le niveau maximal des titres à inclure dans les plans ou de désactiver complètement les plans de titres.

Pour les signets, le niveau du plan peut être défini dans les options comme valeur par défaut pour tous les signets ou comme valeurs individuelles pour des signets particuliers.

De plus, les plans peuvent être exportés au format XPS en utilisant la même classe [OutlineOptions](./).
## Voir aussi

* Class [OutlineOptions](../../outlineoptions/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
