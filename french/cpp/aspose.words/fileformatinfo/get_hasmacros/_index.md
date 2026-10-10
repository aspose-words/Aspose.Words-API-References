---
title: "Méthode Aspose::Words::FileFormatInfo::get_HasMacros"
linktitle: "get_HasMacros"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::FileFormatInfo::get_HasMacros. Retourne true si ce document contient des macros VBA en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Renvoie **true** si ce document contient des macros VBA.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Exemples



Montre comment vérifier la présence de macros VBA sans charger le document.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## Voir aussi

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
