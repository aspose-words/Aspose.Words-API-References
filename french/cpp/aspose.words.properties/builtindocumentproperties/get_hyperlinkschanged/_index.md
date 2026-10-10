---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged méthode"
linktitle: "get_HyperlinksChanged"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged méthode. Indique si les hyperliens d'un document ont été modifiés en C++."
type: docs
weight: 13500
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Indique si les hyperliens d'un document ont été modifiés.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
```

## Remarques


Aspose.Words ne met pas à jour cette propriété.

## Exemples



Montre comment obtenir les propriétés étendues.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
