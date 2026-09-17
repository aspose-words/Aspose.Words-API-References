---
title: "Aspose::Words::WarningInfoCollection::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WarningInfoCollection::get_Count méthode. Obtient le nombre d'éléments contenus dans la collection en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Obtient le nombre d’éléments contenus dans la collection.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


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

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
