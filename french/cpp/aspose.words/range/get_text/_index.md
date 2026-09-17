---
title: "Méthode Aspose::Words::Range::get_Text"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Range::get_Text. Obtient le texte de la plage en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Obtient le texte de la plage.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Remarques


La chaîne retournée comprend tous les caractères de contrôle et spéciaux comme décrit dans [ControlChar](../../controlchar/).

## Exemples



Montre comment obtenir le contenu texte de tous les nœuds couverts par une plage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Voir aussi

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
