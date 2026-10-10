---
title: "Méthode Aspose::Words::BuildVersionInfo::get_Product"
linktitle: "get_Product"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::BuildVersionInfo::get_Product. Obtient le nom complet du produit en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Obtient le nom complet du produit.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Exemples



Montre comment afficher les informations sur votre version installée d'Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Voir aussi

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
