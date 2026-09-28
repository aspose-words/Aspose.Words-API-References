---
title: "Aspose::Words::Document::GetPageInfo метод"
linktitle: "GetPageInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::GetPageInfo метод. Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или рендеринга в C++."
type: docs
weight: 62000
url: /ru/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или визуализации.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int32_t | Нумерация страниц начинается с 0. |

## Примеры



Показывает, как проверить, находится ли страница в цвете или нет.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Проверьте, что первая страница документа не окрашена.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## См. также

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
