---
title: "Aspose::Words::NodeList::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeList::idx_get метод. Получает узел по заданному индексу в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Получает узел по заданному индексу.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в списке узлов. |
## Примечания


Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 — предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается нулевая ссылка.

## См. также

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
