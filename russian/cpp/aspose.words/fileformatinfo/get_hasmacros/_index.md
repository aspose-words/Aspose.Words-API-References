---
title: "Метод Aspose::Words::FileFormatInfo::get_HasMacros"
linktitle: "get_HasMacros"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::FileFormatInfo::get_HasMacros. Возвращает true, если данный документ содержит макросы VBA в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Возвращает **true**, если документ содержит макросы VBA.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Примеры



Показывает, как проверить наличие макросов VBA без загрузки документа.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## См. также

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
