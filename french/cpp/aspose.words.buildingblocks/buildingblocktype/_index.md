---
title: "Aspose::Words::BuildingBlocks::BuildingBlockType enum"
linktitle: "BuildingBlockType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockType enum. Spécifie un type de bloc de construction. Le type peut affecter la visibilité et le comportement du bloc de construction dans Microsoft Word en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enum


Spécifie un type de building block. Le type peut affecter la visibilité et le comportement du building block dans Microsoft Word.

```cpp
enum class BuildingBlockType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucune information de type n'est spécifiée pour le bloc de construction. |
| AutomaticallyReplaceNameWithContent | 1 | Permet au bloc de construction d'être automatiquement inséré dans le document chaque fois que son nom est saisi dans une application. |
| StructuredDocumentTagPlaceholderText | 2 | Le bloc de construction est un texte d'espace réservé de balise de document structuré. |
| FormFieldHelpText | 3 | Le bloc de construction est un texte d'aide de champ de formulaire. |
| Normal | 4 | Le bloc de construction est une entrée de document de glossaire normale (c.-à-d. régulière). |
| AutoCorrect | 5 | Le bloc de construction est associé aux outils d'orthographe et de grammaire. |
| AutoText | 6 | Le bloc de construction est une entrée AutoText. |
| Tous | 7 | Le bloc de construction est associé à tous les types. |
| Default | n/a | Enregistrer sous [None](./). |

## Remarques


Correspond au type **ST_DocPartType** dans OOXML.

## Voir aussi

* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
