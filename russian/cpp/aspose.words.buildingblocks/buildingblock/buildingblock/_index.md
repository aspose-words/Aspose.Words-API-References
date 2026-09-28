---
title: "конструктор Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock"
linktitle: "BuildingBlock"
second_title: "Справочник API Aspose.Words для C++"
description: "конструктор Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock. Инициализирует новый экземпляр этого класса в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.buildingblocks/buildingblock/buildingblock/
---
## BuildingBlock::BuildingBlock constructor


Инициализирует новый экземпляр этого класса.

```cpp
Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock(const System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> &glossaryDoc)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| glossaryDoc | const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\& | Документ‑владелец. |
## Примечания


Когда [BuildingBlock](../) создаётся, он принадлежит указанному документу глоссария, но ещё не является частью документа глоссария и [ParentNode](../../../aspose.words/node/get_parentnode/) имеет значение **null**.

Чтобы добавить [BuildingBlock](../) к [GlossaryDocument](../../glossarydocument/) используйте [AppendChild``1()](../).

## См. также

* Class [GlossaryDocument](../../glossarydocument/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
