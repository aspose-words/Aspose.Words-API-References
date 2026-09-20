---
title: "Aspose::Words::BuildVersionInfo class"
linktitle: "BuildVersionInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BuildVersionInfo class. Предоставляет информацию о текущем названии продукта и его версии. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Предоставляет информацию о текущем названии продукта и версии. Чтобы узнать больше, посетите статью документации [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## Методы

| Метод | Описание |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Возвращает полное название продукта. |
| static [get_Version](./get_version/)() | Возвращает версию продукта. |

## Примеры



Показывает, как отобразить информацию о установленной версии Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
