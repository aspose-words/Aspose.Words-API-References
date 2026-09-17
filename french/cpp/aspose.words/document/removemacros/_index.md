---
title: "Aspose::Words::Document::RemoveMacros méthode"
linktitle: "RemoveMacros"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::RemoveMacros méthode. Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commandes du document en C++."
type: docs
weight: 69000
url: /fr/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commandes du document.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Remarques


En supprimant toutes les macros d'un document, vous pouvez vous assurer que le document ne contient aucun virus macro.

## Exemples



Montre comment supprimer toutes les macros d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Supprime le projet VBA du document, ainsi que toutes ses macros.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
