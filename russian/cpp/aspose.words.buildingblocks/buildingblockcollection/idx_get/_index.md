---
title: "Метод Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get. Извлекает строительный блок по заданному индексу в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.buildingblocks/buildingblockcollection/idx_get/
---
## BuildingBlockCollection::idx_get method


Получает строительный блок по указанному индексу.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в списке строительных блоков. |
## Примечания


Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 — предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается нулевая ссылка.

## См. также

* Class [BuildingBlock](../../buildingblock/)
* Class [BuildingBlockCollection](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
