---
title: "Метод Aspose::Words::BuildVersionInfo::get_Version"
linktitle: "get_Version"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BuildVersionInfo::get_Version. Получает версию продукта в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Возвращает версию продукта.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Примечания


Версия продукта имеет формат "Major.Minor.Hotfix.0".

## Примеры



Показывает, как отобразить информацию о установленной версии Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## См. также

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
