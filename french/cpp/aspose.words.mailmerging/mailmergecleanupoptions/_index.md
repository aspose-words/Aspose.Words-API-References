---
title: "Enum Aspose::Words::MailMerging::MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Enum Aspose::Words::MailMerging::MailMergeCleanupOptions. Spécifie les options qui déterminent quels éléments sont supprimés lors du publipostage en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Spécifie les options qui déterminent quels éléments sont supprimés lors de la fusion de courrier.

```cpp
enum class MailMergeCleanupOptions
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Spécifie une valeur par défaut. |
| RemoveEmptyParagraphs | 1 | Spécifie si les paragraphes contenant des champs de publipostage sans données doivent être supprimés du document. Lorsque cette option est activée, les paragraphes contenant des champs de début et de fin de région qui sont autrement vides sont également supprimés. |
| RemoveUnusedRegions | 2 | Spécifie si les régions de publipostage inutilisées doivent être supprimées du document. |
| RemoveUnusedFields | 4 | Spécifie si les champs de fusion inutilisés doivent être supprimés du document. |
| RemoveContainingFields | 8 | Spécifie si les champs qui contiennent des champs de fusion (par exemple, les IF) doivent être supprimés du document si les champs de fusion imbriqués sont supprimés. |
| RemoveStaticFields | 16 | Spécifie si les champs statiques doivent être supprimés du document. Les champs statiques sont des champs dont les résultats restent les mêmes quel que soit le changement du document. [Fields](../../aspose.words.fields/), qui ne stockent pas leurs résultats dans un document et sont calculés à la volée (comme [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), etc.) ne sont pas considérés comme statiques. |
| RemoveEmptyTableRows | 32 | Spécifie si les lignes vides contenant des régions de publipostage doivent être supprimées du document. |
| RemoveEmptyTables | 64 | Spécifie s'il faut supprimer du document les tables contenant des régions de publipostage qui ont été supprimées en utilisant soit l'option [RemoveUnusedRegions](./), soit l'option [RemoveEmptyTableRows](./). |

## Voir aussi

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
