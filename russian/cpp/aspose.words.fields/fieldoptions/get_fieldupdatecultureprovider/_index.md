---
title: "Метод Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider. Получает или задает поставщик, который возвращает объект культуры, специфичный для каждого отдельного поля в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Получает или задает поставщика, который возвращает объект культуры, специфичный для каждого отдельного поля.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Примечания


Поставщик запрашивается, когда значение [FieldUpdateCultureSource](../get_fieldupdateculturesource/) равно [FieldCode](../../fieldupdateculturesource/).

Если поставщик присутствует, то возвращаемый им объект культуры используется для обновления поля. В противном случае используется системная культура.
## См. также

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
