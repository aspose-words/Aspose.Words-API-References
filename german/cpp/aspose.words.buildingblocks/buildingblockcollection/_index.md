---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection Klasse"
linktitle: "BuildingBlockCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection Klasse. Eine Sammlung von BuildingBlock-Objekten im Dokument. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


Eine Sammlung von [BuildingBlock](../buildingblock/) Objekten im Dokument. Weitere Informationen finden Sie im Artikel zur [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) Dokumentation.

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft einen Baustein am angegebenen Index ab. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](./toarray/)() | Kopiert alle Bausteine aus der Sammlung in ein neues Array von Bausteinen. |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Instanzen dieser Klasse direkt. Um auf eine Sammlung von Bausteinen zuzugreifen, verwenden Sie die Eigenschaft [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## Siehe auch

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
