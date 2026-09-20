---
title: "Aspose::Words::Rendering::PageInfo::get_Colored метод"
linktitle: "get_Colored"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::PageInfo::get_Colored метод. Возвращает true, если страница содержит цветное содержимое в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Возвращает **true**, если страница содержит цветное содержимое.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Примеры



Показывает, как проверить, находится ли страница в цвете или нет.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Проверьте, что первая страница документа не окрашена.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## См. также

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
