---
title: "Aspose::Words::WarningInfoCollection::get_Count метод"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WarningInfoCollection::get_Count метод. Возвращает количество элементов, содержащихся в коллекции, в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Получает количество элементов, содержащихся в коллекции.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


## Примеры



Показывает, как получать предупреждения о неподдерживаемых форматах.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## См. также

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
