---
title: "Aspose::Words::Document::RemoveBlankPages метод"
linktitle: "RemoveBlankPages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::RemoveBlankPages метод. Удаляет пустые страницы из документа в C++."
type: docs
weight: 67500
url: /ru/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Удаляет пустые страницы из документа.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

Список номеров страниц был признан пустым и удалён.

## Примеры



Показывает, как удалить пустые страницы из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
