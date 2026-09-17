---
title: "Méthode Aspose::Words::BuildVersionInfo::get_Version"
linktitle: "get_Version"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::BuildVersionInfo::get_Version. Obtient la version du produit en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Obtient la version du produit.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Remarques


La version du produit est au format "Major.Minor.Hotfix.0".

## Exemples



Montre comment afficher les informations sur votre version installée d'Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Voir aussi

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
