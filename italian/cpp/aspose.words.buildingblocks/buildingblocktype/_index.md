---
title: "Aspose::Words::BuildingBlocks::BuildingBlockType enum"
linktitle: "BuildingBlockType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockType enum. Specifica un tipo di blocco di costruzione. Il tipo potrebbe influire sulla visibilità e sul comportamento del blocco di costruzione in Microsoft Word in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enum


Specifica un tipo di building block. Il tipo potrebbe influire sulla visibilità e sul comportamento del building block in Microsoft Word.

```cpp
enum class BuildingBlockType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Non è specificata alcuna informazione sul tipo per il blocco di costruzione. |
| AutomaticallyReplaceNameWithContent | 1 | Consente al blocco di costruzione di essere inserito automaticamente nel documento ogni volta che il suo nome viene digitato in un'applicazione. |
| StructuredDocumentTagPlaceholderText | 2 | Il blocco di costruzione è un testo segnaposto di tag di documento strutturato. |
| FormFieldHelpText | 3 | Il blocco di costruzione è un testo di aiuto per il campo modulo. |
| Normale | 4 | Il blocco di costruzione è una voce normale (cioè regolare) del documento glossario. |
| AutoCorrect | 5 | Il blocco di costruzione è associato agli strumenti di ortografia e grammatica. |
| AutoText | 6 | Il blocco di costruzione è una voce AutoText. |
| Tutti | 7 | Il blocco di costruzione è associato a tutti i tipi. |
| Default | n/a | Salva come [None](./). |

## Note


Corrisponde al tipo **ST_DocPartType** in OOXML.

## Vedi anche

* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
