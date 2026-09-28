---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title метод"
linktitle: "get_Title"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title метод. Указывает дружественное имя, связанное с этим SDT. Не может быть null в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


Указывает удобочитаемое имя, связанное с этим **SDT**. Не может быть null.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
```


## Примеры



Показывает, как получить тег структурированного документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Получить тег структурированного документа по Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Получить тег структурированного документа или диапазонный тег по Title.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## См. также

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
