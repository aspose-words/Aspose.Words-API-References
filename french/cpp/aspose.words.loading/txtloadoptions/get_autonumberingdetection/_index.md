---
title: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection méthode"
linktitle: "get_AutoNumberingDetection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection méthode. Obtient ou définit une valeur booléenne indiquant si la détection automatique de la numérotation sera effectuée lors du chargement d'un document. La valeur par défaut est true en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Obtient ou définit une valeur booléenne indiquant si la détection automatique de la numérotation sera effectuée lors du chargement d'un document. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Exemples



Montre comment désactiver la détection automatique de la numérotation.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## Voir aussi

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
