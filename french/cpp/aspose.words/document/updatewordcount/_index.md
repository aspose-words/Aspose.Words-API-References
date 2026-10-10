---
title: "Méthode Aspose::Words::Document::UpdateWordCount"
linktitle: "UpdateWordCount"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::UpdateWordCount. Met à jour les propriétés de comptage des mots du document en C++."
type: docs
weight: 101000
url: /fr/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


Met à jour les propriétés de comptage de mots du document.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## Remarques


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

Notez que [UpdateWordCount](./) ne met pas à jour les propriétés du nombre de lignes et de pages. Utilisez la surcharge de [UpdateWordCount](./) et passez la valeur **true** en paramètre pour le faire.

Lorsque vous utilisez une version d'évaluation, le filigrane d'évaluation sera également inclus dans le comptage des mots.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


Met à jour les propriétés de comptage des mots du document, met éventuellement à jour la propriété [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/).

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| updateLinesCount | bool | **true** si le nombre de lignes dans le document doit être calculé. |

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
