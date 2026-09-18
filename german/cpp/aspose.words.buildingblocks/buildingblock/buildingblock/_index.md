---
title: "Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock Konstruktor"
linktitle: "BuildingBlock"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock Konstruktor. Initialisiert eine neue Instanz dieser Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.buildingblocks/buildingblock/buildingblock/
---
## BuildingBlock::BuildingBlock constructor


Initialisiert eine neue Instanz dieser Klasse.

```cpp
Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock(const System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> &glossaryDoc)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| glossaryDoc | const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\& | Das Eigentümerdokument. |
## Hinweise


Wenn ein [BuildingBlock](../) erstellt wird, gehört er zum angegebenen Glossar-Dokument, ist jedoch noch nicht Teil des Glossar-Dokuments und [ParentNode](../../../aspose.words/node/get_parentnode/) ist **null**.

Um ein [BuildingBlock](../) an ein [GlossaryDocument](../../glossarydocument/) anzuhängen, verwenden Sie [AppendChild``1()](../).

## Siehe auch

* Class [GlossaryDocument](../../glossarydocument/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
