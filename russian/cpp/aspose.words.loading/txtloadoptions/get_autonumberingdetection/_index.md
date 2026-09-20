---
title: "Метод Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection"
linktitle: "get_AutoNumberingDetection"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection. Получает или задает логическое значение, указывающее, будет ли выполнено автоматическое определение нумерации при загрузке документа. Значение по умолчанию — true в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Получает или задает логическое значение, указывающее, будет ли выполнено автоматическое обнаружение нумерации при загрузке документа. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Примеры



Показывает, как отключить автоматическое определение нумерации.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## См. также

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
