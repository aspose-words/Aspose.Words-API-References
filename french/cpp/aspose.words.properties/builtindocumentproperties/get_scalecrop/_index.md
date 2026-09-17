---
title: "Méthode Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop"
linktitle: "get_ScaleCrop"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop. Indique si la vignette du document est recadrée ou mise à l'échelle pour s'adapter à l'affichage en C++."
type: docs
weight: 24500
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Indique si la vignette du document est recadrée ou mise à l'échelle pour s'adapter à l'affichage.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
