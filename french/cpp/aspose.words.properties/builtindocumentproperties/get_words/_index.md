---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Words méthode"
linktitle: "get_Words"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Words méthode. Représente une estimation du nombre de mots dans le document en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_words/
---
## BuiltInDocumentProperties::get_Words method


Représente une estimation du nombre de mots dans le document.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Words()
```

## Remarques


Aspose.Words met à jour cette propriété lorsque vous appelez [UpdateWordCount](../../../aspose.words/document/updatewordcount/).

## Exemples



Montre comment mettre à jour toutes les étiquettes de liste dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words ne suit pas les métriques du document comme celles-ci en temps réel.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Pour obtenir des valeurs précises pour trois de ces propriétés, nous devrons les mettre à jour manuellement.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Pour le nombre de lignes, nous devrons appeler une surcharge spécifique de la méthode de mise à jour.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
