---
title: "Aspose::Words::WarningInfoCollection::idx_get méthode"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WarningInfoCollection::idx_get méthode. Obtient un élément à l'index spécifié en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/warninginfocollection/idx_get/
---
## WarningInfoCollection::idx_get method


Obtient un élément à l'index spécifié.

```cpp
System::SharedPtr<Aspose::Words::WarningInfo> Aspose::Words::WarningInfoCollection::idx_get(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Index de l'élément basé sur zéro. |

## Exemples



Montre comment obtenir des avertissements concernant les formats non pris en charge.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## Voir aussi

* Class [WarningInfo](../../warninginfo/)
* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
