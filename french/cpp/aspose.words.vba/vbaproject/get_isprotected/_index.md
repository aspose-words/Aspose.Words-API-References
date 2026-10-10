---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected méthode"
linktitle: "get_IsProtected"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected méthode. Indique si le VbaProject est protégé par mot de passe en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


Indique si le [VbaProject](../) est protégé par mot de passe.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Exemples



Indique si le [VbaProject](../) est protégé par mot de passe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## Voir aussi

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
