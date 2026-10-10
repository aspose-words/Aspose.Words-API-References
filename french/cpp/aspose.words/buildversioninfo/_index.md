---
title: "Aspose::Words::BuildVersionInfo classe"
linktitle: "BuildVersionInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BuildVersionInfo classe. Fournit des informations sur le nom et la version actuels du produit. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Fournit des informations sur le nom et la version du produit actuel. Pour en savoir plus, consultez l'article de documentation [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Obtient le nom complet du produit. |
| static [get_Version](./get_version/)() | Obtient la version du produit. |

## Exemples



Montre comment afficher les informations sur votre version installée d'Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
