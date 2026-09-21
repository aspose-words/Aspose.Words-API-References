---
title: "Klassen Aspose::Words::BuildingBlocks::BuildingBlockCollection"
linktitle: "BuildingBlockCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Klassen Aspose::Words::BuildingBlocks::BuildingBlockCollection. En samling av BuildingBlock‑objekt i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


En samling av [BuildingBlock](../buildingblock/)‑objekt i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från denna samling och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Avgör om en nod finns i samlingen. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Hämtar antalet noder i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett byggblock på det angivna indexet. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](./toarray/)() | Kopierar alla byggblock från samlingen till en ny array av byggblock. |
| static [Type](./type/)() |  |
## Anmärkningar


Du skapar inte instanser av den här klassen direkt. För att komma åt en samling av byggblock, använd egenskapen [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## Se även

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
